---
title: imapisupportgetmemallocroutines
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316563"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="004c6-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="004c6-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="004c6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="004c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="004c6-105">MAPI メモリ割り当て関数および割り当て解除関数 ([MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)) のアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="004c6-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="004c6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="004c6-106">Parameters</span></span>

 <span data-ttu-id="004c6-107">_lppallocatebuffer_</span><span class="sxs-lookup"><span data-stu-id="004c6-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="004c6-108">読み上げ**MAPIAllocateBuffer**関数へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="004c6-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="004c6-109">**MAPIAllocateBuffer**はメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="004c6-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="004c6-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="004c6-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="004c6-111">読み上げ**MAPIAllocateMore**関数へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="004c6-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="004c6-112">**MAPIAllocateMore**は、 **MAPIAllocateBuffer**を使用して最初に割り当てられたメモリの追加メモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="004c6-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="004c6-113">_lppfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="004c6-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="004c6-114">読み上げ**MAPIFreeBuffer**関数へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="004c6-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="004c6-115">**MAPIFreeBuffer**はメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="004c6-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="004c6-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="004c6-116">Return value</span></span>

<span data-ttu-id="004c6-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="004c6-117">S_OK</span></span> 
  
> <span data-ttu-id="004c6-118">関数のアドレスが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="004c6-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="004c6-119">解説</span><span class="sxs-lookup"><span data-stu-id="004c6-119">Remarks</span></span>

<span data-ttu-id="004c6-120">**imapisupport:: getmemallocroutines**メソッドは、すべてのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="004c6-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="004c6-121">サービスプロバイダーは、 **getmemallocroutines**を呼び出して、初期化関数 ( [abproviderinit](abproviderinit.md)、 [msproviderinit](msproviderinit.md)、または[xps プロバイダー init](xpproviderinit.md)) に渡される3つのメモリ割り当て関数のアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="004c6-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="004c6-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="004c6-122">See also</span></span>



[<span data-ttu-id="004c6-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="004c6-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="004c6-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="004c6-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="004c6-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="004c6-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="004c6-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="004c6-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

