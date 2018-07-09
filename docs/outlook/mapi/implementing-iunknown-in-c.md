---
title: C の IUnknown の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d12201d8476d15021e896a44797ae5fc21178802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800946"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="58a5f-103">C の IUnknown の実装</span><span class="sxs-lookup"><span data-stu-id="58a5f-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="58a5f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58a5f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58a5f-105">C の[IUnknown::QueryInterface](http://msdn.microsoft.com/ja-jp/library/ms682521%28v=VS.85%29.aspx)メソッドの実装は、C++ の実装に非常に似ています。</span><span class="sxs-lookup"><span data-stu-id="58a5f-105">Implementations of the [IUnknown::QueryInterface](http://msdn.microsoft.com/ja-jp/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="58a5f-106">実装に 2 つの基本的な手順があります。</span><span class="sxs-lookup"><span data-stu-id="58a5f-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="58a5f-107">パラメーターを検証しています。</span><span class="sxs-lookup"><span data-stu-id="58a5f-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="58a5f-108">オブジェクトによってサポートされているインターフェイスの一覧に対して要求されたインターフェイスの id を確認し、E_NO_INTERFACE の値または有効なインターフェイス ポインターのいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="58a5f-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="58a5f-109">インターフェイス ポインターが返される場合、実装を使用、参照カウントをインクリメントする[IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="58a5f-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="58a5f-110">**QueryInterface**を c 言語での実装と C++ の間の主な違いは、C のバージョンで追加の最初のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="58a5f-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="58a5f-111">パラメーター リストには、オブジェクトへのポインターを追加するため、 **QueryInterface**の C の実装には C++ 実装より多くのパラメーターの検証が必要です。</span><span class="sxs-lookup"><span data-stu-id="58a5f-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="58a5f-112">インターフェイス識別子を確認、参照カウントをインクリメントして、オブジェクトのポインターを返すのためのロジックは、両方の言語で同等でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="58a5f-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="58a5f-113">次のコード例では、状態オブジェクトの**QueryInterface**を C で実装する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="58a5f-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="58a5f-114">C で**AddRef**メソッドの実装は、C++ の実装に似ていますが、C のバージョンよりもより複雑な C の実装[が](http://msdn.microsoft.com/ja-jp/library/ms682317%28v=VS.85%29.aspx)このメソッドを取得します。</span><span class="sxs-lookup"><span data-stu-id="58a5f-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](http://msdn.microsoft.com/ja-jp/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="58a5f-115">オブジェクトを解放することに関連する機能の多くに組み込むこと、C++ のコンス トラクターとデストラクター、および C には、このようなメカニズムがないためにです。</span><span class="sxs-lookup"><span data-stu-id="58a5f-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="58a5f-116">**Release**メソッドでこの機能をすべて含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="58a5f-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="58a5f-117">また、追加のパラメーターとその明示的な v テーブル、複数の検証が必要です。</span><span class="sxs-lookup"><span data-stu-id="58a5f-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="58a5f-118">次の**AddRef**メソッドの呼び出しは、状態オブジェクトの C の標準的な実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="58a5f-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="58a5f-119">次のコード例では、**リリース**の C 状態のオブジェクトの一般的な実装を示します。</span><span class="sxs-lookup"><span data-stu-id="58a5f-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="58a5f-120">デクリメントされた後、参照カウントが 0 の場合、C 状態のオブジェクトの実装は、次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58a5f-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="58a5f-121">オブジェクトに保持されているポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="58a5f-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="58a5f-122">Vtable をデバッグの場合は、まだ**リリース**と呼ばれるオブジェクトのユーザーがオブジェクトを使用しようとする継続を促進する、NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="58a5f-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="58a5f-123">オブジェクトを解放するために**MAPIFreeBuffer**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="58a5f-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="58a5f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="58a5f-124">See also</span></span>

- [<span data-ttu-id="58a5f-125">MAPI オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="58a5f-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="58a5f-126">IUnknown インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="58a5f-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

