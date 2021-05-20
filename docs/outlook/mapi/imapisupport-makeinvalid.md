---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427494"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="cebe9-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="cebe9-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="cebe9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cebe9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cebe9-105">オブジェクトを使用不可としてマークします。</span><span class="sxs-lookup"><span data-stu-id="cebe9-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="cebe9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cebe9-106">Parameters</span></span>

 <span data-ttu-id="cebe9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cebe9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cebe9-108">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cebe9-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cebe9-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="cebe9-109">_lpObject_</span></span>
  
> <span data-ttu-id="cebe9-110">[in]無効になるオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cebe9-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="cebe9-111">オブジェクトのインターフェイスは **、IUnknown から派生する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="cebe9-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="cebe9-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="cebe9-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="cebe9-113">[in]オブジェクトの現在の参照カウント。</span><span class="sxs-lookup"><span data-stu-id="cebe9-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="cebe9-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="cebe9-114">_cMethods_</span></span>
  
> <span data-ttu-id="cebe9-115">[in]オブジェクトの vtable 内のメソッドの数。</span><span class="sxs-lookup"><span data-stu-id="cebe9-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cebe9-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="cebe9-116">Return value</span></span>

<span data-ttu-id="cebe9-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="cebe9-117">S_OK</span></span> 
  
> <span data-ttu-id="cebe9-118">オブジェクトが使用不能として正常にマークされました。</span><span class="sxs-lookup"><span data-stu-id="cebe9-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cebe9-119">注釈</span><span class="sxs-lookup"><span data-stu-id="cebe9-119">Remarks</span></span>

<span data-ttu-id="cebe9-120">**IMAPISupport::MakeInvalid メソッド** は、すべてのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="cebe9-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="cebe9-121">無効になるオブジェクトは **、IUnknown インターフェイスまたは IUnknown** から派生したインターフェイスから派生 **している必要があります**。</span><span class="sxs-lookup"><span data-stu-id="cebe9-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="cebe9-122">**MakeInvalid** は、オブジェクトの vtable を **、IUnknown::AddRef** メソッドと **IUnknown::Release** メソッドが期待通り実行する類似のサイズのスタブ vtable に置き換え、オブジェクトを使用不能としてマークします。</span><span class="sxs-lookup"><span data-stu-id="cebe9-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="cebe9-123">ただし、他のメソッドは失敗し、値が返MAPI_E_INVALID_OBJECT。</span><span class="sxs-lookup"><span data-stu-id="cebe9-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cebe9-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="cebe9-124">Notes to callers</span></span>

<span data-ttu-id="cebe9-125">サービス プロバイダーとメッセージ サービスは、通常、シャットダウン時に **MakeInvalid** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cebe9-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="cebe9-126">ただし **、MakeInvalid** は、いつでも呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="cebe9-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="cebe9-127">たとえば、クライアントが一部のサブオブジェクトを解放せずにオブジェクトを解放する場合は **、MakeInvalid** をすぐに呼び出して、それらのサブオブジェクトを解放できます。</span><span class="sxs-lookup"><span data-stu-id="cebe9-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="cebe9-128">無効にしようとするオブジェクトを所有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cebe9-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="cebe9-129">長さ 16 バイト以上で、vtable には少なくとも 3 つのメソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="cebe9-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="cebe9-130">**MakeInvalid** を呼び出して、関連付けられたデータ構造の破棄など、通常はオブジェクトのリリース中に実行されるシャットダウン作業を実行できます。</span><span class="sxs-lookup"><span data-stu-id="cebe9-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="cebe9-131">MAPI は [MAPIFreeBuffer](mapifreebuffer.md) を呼び出してオブジェクトを解放することでメモリを解放しますので、オブジェクトをサポートするコードをメモリに保持する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cebe9-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="cebe9-132">リソースを解放し **、MakeInvalid を呼び出** し、無効化されたオブジェクトを無視できます。</span><span class="sxs-lookup"><span data-stu-id="cebe9-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cebe9-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="cebe9-133">See also</span></span>



[<span data-ttu-id="cebe9-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="cebe9-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="cebe9-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cebe9-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

