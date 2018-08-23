---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c3ec99e4e284ca2cdc4fba8fcf53a6c5741594cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577815"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="37e45-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="37e45-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="37e45-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37e45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37e45-105">MAPI メモリの割り当てと割り当て解除関数 ([MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)) のアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="37e45-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="37e45-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37e45-106">Parameters</span></span>

 <span data-ttu-id="37e45-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="37e45-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="37e45-108">[out]**MAPIAllocateBuffer**関数へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37e45-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="37e45-109">**MAPIAllocateBuffer**は、メモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="37e45-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="37e45-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="37e45-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="37e45-111">[out]**MAPIAllocateMore**関数へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37e45-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="37e45-112">**MAPIAllocateMore**は、 **MAPIAllocateBuffer**を使用して割り当てられているメモリの追加のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="37e45-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="37e45-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="37e45-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="37e45-114">[out]**MAPIFreeBuffer**関数へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37e45-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="37e45-115">**MAPIFreeBuffer**は、メモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="37e45-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="37e45-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="37e45-116">Return value</span></span>

<span data-ttu-id="37e45-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="37e45-117">S_OK</span></span> 
  
> <span data-ttu-id="37e45-118">関数のアドレスが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="37e45-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37e45-119">注釈</span><span class="sxs-lookup"><span data-stu-id="37e45-119">Remarks</span></span>

<span data-ttu-id="37e45-120">サポートのすべてのオブジェクトの**IMAPISupport::GetMemAllocRoutines**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="37e45-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="37e45-121">サービス プロバイダーは、 [ABProviderInit](abproviderinit.md)、 [MSProviderInit](msproviderinit.md)、( [XPProviderInit](xpproviderinit.md)) は、その初期化関数に渡される 3 つのメモリ割り当て関数のアドレスを取得するのには**GetMemAllocRoutines**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="37e45-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="37e45-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="37e45-122">See also</span></span>



[<span data-ttu-id="37e45-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="37e45-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="37e45-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="37e45-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="37e45-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="37e45-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="37e45-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="37e45-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

