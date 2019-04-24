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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="4c4a7-103">C での IUnknown の実装</span><span class="sxs-lookup"><span data-stu-id="4c4a7-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="4c4a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c4a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c4a7-105">c での[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドの実装は、C++ 実装によく似ています。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-105">Implementations of the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="4c4a7-106">実装には、次の2つの基本的な手順があります。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="4c4a7-107">パラメーターを検証します。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="4c4a7-108">オブジェクトでサポートされているインターフェイスのリストに対して要求されたインターフェイスの識別子をチェックし、E_NO_INTERFACE 値または有効なインターフェイスポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="4c4a7-109">インターフェイスポインターが返された場合は、参照カウントをインクリメントするために、実装で[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出す必要もあります。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="4c4a7-110">c および C++ での**QueryInterface**の実装の主な違いは、c バージョンの最初のパラメーターの追加です。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="4c4a7-111">オブジェクトポインターがパラメータリストに追加されているため、 **QueryInterface**の C 実装は C++ 実装よりも多くのパラメータ検証を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="4c4a7-112">インターフェイス識別子を確認し、参照カウントを増やして、オブジェクトポインターを返すロジックは、両方の言語で同一である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="4c4a7-113">次のコード例は、ステータスオブジェクトの C で**QueryInterface**を実装する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="4c4a7-114">c での**AddRef**メソッドの実装は c++ 実装に似ていますが、 [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドの C 実装は、c++ のバージョンよりも凝ったものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="4c4a7-115">これは、オブジェクトを解放するための機能の多くが C++ のコンストラクタおよびデストラクターに組み込まれる可能性があるため、C にはそのような機構がありません。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="4c4a7-116">この機能はすべて、 **Release**メソッドに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="4c4a7-117">また、追加のパラメーターとその明示的な vtable があるため、より多くの検証が必要になります。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="4c4a7-118">次の**AddRef**メソッドの呼び出しは、status オブジェクトの一般的な C 実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="4c4a7-119">次のコード例は、C status オブジェクトの**リリース**の一般的な実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="4c4a7-120">参照カウントがデクリメントされた後に0の場合、C status オブジェクトの実装では、次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="4c4a7-121">オブジェクトへのすべての保持ポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="4c4a7-122">vtable を NULL に設定して、オブジェクトのユーザーが**Release**という名前のオブジェクトを引き続き使用していた場合のデバッグを容易にします。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="4c4a7-123">**MAPIFreeBuffer**を呼び出して、オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="4c4a7-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="4c4a7-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c4a7-124">See also</span></span>

- [<span data-ttu-id="4c4a7-125">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="4c4a7-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="4c4a7-126">IUnknown インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="4c4a7-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

