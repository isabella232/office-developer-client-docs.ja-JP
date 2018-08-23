---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801522"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="edad4-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="edad4-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="edad4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="edad4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="edad4-105">メモリ バッファーを再割り当ています。</span><span class="sxs-lookup"><span data-stu-id="edad4-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="edad4-106">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数で使用されます。</span><span class="sxs-lookup"><span data-stu-id="edad4-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="edad4-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="edad4-107">Header file:</span></span>  <br/> |<span data-ttu-id="edad4-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="edad4-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="edad4-109">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="edad4-109">Called by:</span></span>  <br/> |<span data-ttu-id="edad4-110">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="edad4-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="edad4-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edad4-111">Parameters</span></span>

 <span data-ttu-id="edad4-112">_lpv_</span><span class="sxs-lookup"><span data-stu-id="edad4-112">_lpv_</span></span>
  
> <span data-ttu-id="edad4-113">再割り当てするメモリへのポインター。</span><span class="sxs-lookup"><span data-stu-id="edad4-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="edad4-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="edad4-114">_ulSize_</span></span>
  
> <span data-ttu-id="edad4-115">割り当てられるバッファーのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="edad4-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="edad4-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="edad4-116">_lppv_</span></span>
  
> <span data-ttu-id="edad4-117">返されるバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="edad4-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edad4-118">注釈</span><span class="sxs-lookup"><span data-stu-id="edad4-118">Remarks</span></span>

 <span data-ttu-id="edad4-119">**MAPIReallocateBuffer**は、新しい要求されたサイズのメモリ ブロックを割り当て、この新しいメモリのブロックに渡されるバッファーの内容をコピーします。</span><span class="sxs-lookup"><span data-stu-id="edad4-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="edad4-120">渡されたメモリのブロックには、内部ポインターが含まれている場合、ポインターが新しい位置に合わせて変更されません。</span><span class="sxs-lookup"><span data-stu-id="edad4-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="edad4-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="edad4-121">See also</span></span>



[<span data-ttu-id="edad4-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="edad4-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

