---
title: C での IUnknown の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3c634defcad76755fc6604a23d2091bb21e15111
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391445"
---
# <a name="implementing-iunknown-in-c"></a>C での IUnknown の実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
C の[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドの実装は、C++ の実装に非常に似ています。 実装に 2 つの基本的な手順があります。 
  
1. パラメーターを検証しています。
    
2. オブジェクトによってサポートされているインターフェイスの一覧に対して要求されたインターフェイスの id を確認し、E_NO_INTERFACE の値または有効なインターフェイス ポインターのいずれかを返します。 インターフェイス ポインターが返される場合、実装を使用、参照カウントをインクリメントする[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出す必要があります。 
    
**QueryInterface**を c 言語での実装と C++ の間の主な違いは、C のバージョンで追加の最初のパラメーターです。 パラメーター リストには、オブジェクトへのポインターを追加するため、 **QueryInterface**の C の実装には C++ 実装より多くのパラメーターの検証が必要です。 インターフェイス識別子を確認、参照カウントをインクリメントして、オブジェクトのポインターを返すのためのロジックは、両方の言語で同等でなければなりません。 
  
次のコード例では、状態オブジェクトの**QueryInterface**を C で実装する方法を示します。 
  
```cpp
STDMETHODIMP STATUS_QueryInterface(LPMYSTATUSOBJ lpMyObj, REFIID riid,
                                   LPVOID FAR * lppvObj)
{
    HRESULT hr = hrSuccess;
    // Validate the object pointer.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS )
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Validate other parameters.
    if (!lppvObj)
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Set the output pointer to NULL.
    *lppvObj = NULL;
    // Check the interface identifier.
    if (memcmp(riid, &IID_IUnknown, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIProp, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIStatus, sizeof(IID)))
    {
        hr = ResultFromScode(E_NOINTERFACE);
        return hr;
    }
    // The interface is supported. Increment the reference count and return.
    lpMyObj->lpVtbl->AddRef(lpMyObj);
    *lppvObj = lpMyObj;
    return hr;
}

```

C で**AddRef**メソッドの実装は、C++ の実装に似ていますが、C のバージョンよりもより複雑な C の実装[が](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)このメソッドを取得します。 オブジェクトを解放することに関連する機能の多くに組み込むこと、C++ のコンス トラクターとデストラクター、および C には、このようなメカニズムがないためにです。 **Release**メソッドでこの機能をすべて含める必要があります。 また、追加のパラメーターとその明示的な v テーブル、複数の検証が必要です。 
  
次の**AddRef**メソッドの呼び出しは、状態オブジェクトの C の標準的な実装を示しています。 
  
```cpp
STDMETHODIMP_(ULONG) STATUS_AddRef(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check to see whether it has a lpVtbl object member.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    // Check the method.
    if (STATUS_AddRef != lpMyObj->lpVtbl->AddRef)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = ++lpMyObj->cRef;
    InterlockedDecrement (lpMyObj->cRef);
    return cRef;
}

```

次のコード例では、**リリース**の C 状態のオブジェクトの一般的な実装を示します。 デクリメントされた後、参照カウントが 0 の場合、C 状態のオブジェクトの実装は、次のタスクを実行する必要があります。 
  
- オブジェクトに保持されているポインターを解放します。 
    
- Vtable をデバッグの場合は、まだ**リリース**と呼ばれるオブジェクトのユーザーがオブジェクトを使用しようとする継続を促進する、NULL に設定します。 
    
- オブジェクトを解放するために**MAPIFreeBuffer**を呼び出します。 
    
```cpp
STDMETHODIMP_(ULONG) STATUS_Release(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check the size of the vtable.
    if (!lpMyObj)
    {
        return 1;
    }
    // Check whether the vtable is correct.
    if (lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = --lpMyObj->cRef;
    InterlockedIncrement (lpMyObj->cRef);
    if (cRef == 0)
    {
        lpMyObj->lpVtbl->Release(lpMyObj);
        DeleteCriticalSection(&lpMyObj->cs);
        // Release the IMAPIProp pointer.
        lpMyObj->lpProp->Release(lpMyObj->lpProp);
        lpMyObj->lpVtbl = NULL;
        lpMyObj->lpFreeBuff(lpMyObj);
        return 0;
    }
    return cRef;
}

```

## <a name="see-also"></a>関連項目

- [MAPI オブジェクトの実装](implementing-mapi-objects.md)
- [IUnknown インターフェイスの実装](implementing-the-iunknown-interface.md)

