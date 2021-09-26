---
title: C での IUnknown の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 11c52770251528f58edd09b66fdf855c6669fdf4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620745"
---
# <a name="implementing-iunknown-in-c"></a>C での IUnknown の実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
C の [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) メソッドの実装は、C++ の実装と非常に似ています。 実装には、次の 2 つの基本的な手順があります。 
  
1. パラメーターの検証。
    
2. 要求されたインターフェイスの識別子をオブジェクトでサポートされているインターフェイスの一覧に対してチェックし、E_NO_INTERFACE値または有効なインターフェイス ポインターを返します。 インターフェイス ポインターが返された場合、実装は [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) メソッドを呼び出して参照カウントをインクリメントする必要があります。 
    
C と C++ での **QueryInterface** の実装の主な違いは、C バージョンの追加の最初のパラメーターです。 オブジェクト ポインターがパラメーター リストに追加されるので **、QueryInterface** の C 実装では、C++ 実装よりも多くのパラメーター検証が必要です。 インターフェイス識別子を確認し、参照カウントを増やし、オブジェクト ポインターを返すロジックは、両方の言語で同一である必要があります。 
  
次のコード例は、状態オブジェクトの **QueryInterface** を C で実装する方法を示しています。 
  
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

C の **AddRef** メソッドの実装は C++ 実装に似ていますが [、IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドの C 実装は、C++ バージョンよりも複雑な場合があります。 これは、オブジェクトの解放に関連する機能の多くを C++ コンストラクターとデストラクタに組み込み、C にはそのようなメカニズムがないためです。 この機能はすべて Release メソッドに含める **必要** があります。 また、追加のパラメーターとその明示的な vtable のために、より多くの検証が必要です。 
  
次の **AddRef メソッド** 呼び出しは、状態オブジェクトの一般的な C 実装を示しています。 
  
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

次のコード例は、C 状態オブジェクトの **リリースの** 一般的な実装を示しています。 参照カウントがデクリメント後に 0 の場合、C 状態オブジェクトの実装は次のタスクを実行する必要があります。 
  
- オブジェクトへの保持されているポインターを解放します。 
    
- vtable を NULL に設定すると、Release という名前のオブジェクトのユーザーがまだオブジェクトの使用を試み続けた場合のデバッグが容易になります。 
    
- **MAPIFreeBuffer を呼び出** してオブジェクトを解放します。 
    
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

