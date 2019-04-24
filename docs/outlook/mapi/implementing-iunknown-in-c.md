---
title: C での IUnknown の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3c634defcad76755fc6604a23d2091bb21e15111
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346775"
---
# <a name="implementing-iunknown-in-c"></a>C での IUnknown の実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
c での[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドの実装は、C++ 実装によく似ています。 実装には、次の2つの基本的な手順があります。 
  
1. パラメーターを検証します。
    
2. オブジェクトでサポートされているインターフェイスのリストに対して要求されたインターフェイスの識別子をチェックし、E_NO_INTERFACE 値または有効なインターフェイスポインターを返します。 インターフェイスポインターが返された場合は、参照カウントをインクリメントするために、実装で[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出す必要もあります。 
    
c および C++ での**QueryInterface**の実装の主な違いは、c バージョンの最初のパラメーターの追加です。 オブジェクトポインターがパラメータリストに追加されているため、 **QueryInterface**の C 実装は C++ 実装よりも多くのパラメータ検証を行う必要があります。 インターフェイス識別子を確認し、参照カウントを増やして、オブジェクトポインターを返すロジックは、両方の言語で同一である必要があります。 
  
次のコード例は、ステータスオブジェクトの C で**QueryInterface**を実装する方法を示しています。 
  
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

c での**AddRef**メソッドの実装は c++ 実装に似ていますが、 [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドの C 実装は、c++ のバージョンよりも凝ったものにすることができます。 これは、オブジェクトを解放するための機能の多くが C++ のコンストラクタおよびデストラクターに組み込まれる可能性があるため、C にはそのような機構がありません。 この機能はすべて、 **Release**メソッドに含める必要があります。 また、追加のパラメーターとその明示的な vtable があるため、より多くの検証が必要になります。 
  
次の**AddRef**メソッドの呼び出しは、status オブジェクトの一般的な C 実装を示しています。 
  
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

次のコード例は、C status オブジェクトの**リリース**の一般的な実装を示しています。 参照カウントがデクリメントされた後に0の場合、C status オブジェクトの実装では、次のタスクを実行する必要があります。 
  
- オブジェクトへのすべての保持ポインターを解放します。 
    
- vtable を NULL に設定して、オブジェクトのユーザーが**Release**という名前のオブジェクトを引き続き使用していた場合のデバッグを容易にします。 
    
- **MAPIFreeBuffer**を呼び出して、オブジェクトを解放します。 
    
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

