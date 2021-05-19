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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="87a87-103">C での IUnknown の実装</span><span class="sxs-lookup"><span data-stu-id="87a87-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="87a87-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87a87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87a87-105">C の [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) メソッドの実装は、C++ の実装と非常に似ています。</span><span class="sxs-lookup"><span data-stu-id="87a87-105">Implementations of the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="87a87-106">実装には、次の 2 つの基本的な手順があります。</span><span class="sxs-lookup"><span data-stu-id="87a87-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="87a87-107">パラメーターの検証。</span><span class="sxs-lookup"><span data-stu-id="87a87-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="87a87-108">要求されたインターフェイスの識別子をオブジェクトでサポートされているインターフェイスの一覧に対してチェックし、E_NO_INTERFACE値または有効なインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="87a87-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="87a87-109">インターフェイス ポインターが返された場合、実装は [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) メソッドを呼び出して参照カウントをインクリメントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="87a87-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="87a87-110">C と C++ での **QueryInterface** の実装の主な違いは、C バージョンの追加の最初のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="87a87-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="87a87-111">オブジェクト ポインターがパラメーター リストに追加されるので **、QueryInterface** の C 実装では、C++ 実装よりも多くのパラメーター検証が必要です。</span><span class="sxs-lookup"><span data-stu-id="87a87-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="87a87-112">インターフェイス識別子を確認し、参照カウントを増やし、オブジェクト ポインターを返すロジックは、両方の言語で同一である必要があります。</span><span class="sxs-lookup"><span data-stu-id="87a87-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="87a87-113">次のコード例は、状態オブジェクトの **QueryInterface** を C で実装する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="87a87-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="87a87-114">C の **AddRef** メソッドの実装は C++ 実装に似ていますが [、IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドの C 実装は、C++ バージョンよりも複雑な場合があります。</span><span class="sxs-lookup"><span data-stu-id="87a87-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="87a87-115">これは、オブジェクトの解放に関連する機能の多くを C++ コンストラクターとデストラクタに組み込み、C にはそのようなメカニズムがないためです。</span><span class="sxs-lookup"><span data-stu-id="87a87-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="87a87-116">この機能はすべて Release メソッドに含める **必要** があります。</span><span class="sxs-lookup"><span data-stu-id="87a87-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="87a87-117">また、追加のパラメーターとその明示的な vtable のために、より多くの検証が必要です。</span><span class="sxs-lookup"><span data-stu-id="87a87-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="87a87-118">次の **AddRef メソッド** 呼び出しは、状態オブジェクトの一般的な C 実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="87a87-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="87a87-119">次のコード例は、C 状態オブジェクトの **リリースの** 一般的な実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="87a87-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="87a87-120">参照カウントがデクリメント後に 0 の場合、C 状態オブジェクトの実装は次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87a87-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="87a87-121">オブジェクトへの保持されているポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="87a87-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="87a87-122">vtable を NULL に設定すると、Release という名前のオブジェクトのユーザーがまだオブジェクトの使用を試み続けた場合のデバッグが容易になります。</span><span class="sxs-lookup"><span data-stu-id="87a87-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="87a87-123">**MAPIFreeBuffer を呼び出** してオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="87a87-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="87a87-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="87a87-124">See also</span></span>

- [<span data-ttu-id="87a87-125">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="87a87-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="87a87-126">IUnknown インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="87a87-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

