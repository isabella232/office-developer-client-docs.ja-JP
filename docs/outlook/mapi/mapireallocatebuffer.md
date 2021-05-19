---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435286"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="b1636-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="b1636-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="b1636-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1636-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1636-105">メモリ バッファーを再割り当てします。</span><span class="sxs-lookup"><span data-stu-id="b1636-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="b1636-106">[MAPIAllocateBuffer 関数と共に使用](mapiallocatebuffer.md)されます。</span><span class="sxs-lookup"><span data-stu-id="b1636-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1636-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b1636-107">Header file:</span></span>  <br/> |<span data-ttu-id="b1636-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="b1636-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="b1636-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b1636-109">Called by:</span></span>  <br/> |<span data-ttu-id="b1636-110">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b1636-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="b1636-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1636-111">Parameters</span></span>

 <span data-ttu-id="b1636-112">_lpv_</span><span class="sxs-lookup"><span data-stu-id="b1636-112">_lpv_</span></span>
  
> <span data-ttu-id="b1636-113">割り当て可能なメモリへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b1636-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="b1636-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="b1636-114">_ulSize_</span></span>
  
> <span data-ttu-id="b1636-115">割り当てるバッファーのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="b1636-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="b1636-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="b1636-116">_lppv_</span></span>
  
> <span data-ttu-id="b1636-117">返される割り当てられたバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b1636-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1636-118">注釈</span><span class="sxs-lookup"><span data-stu-id="b1636-118">Remarks</span></span>

 <span data-ttu-id="b1636-119">**MAPIReallocateBuffer** は、要求されたサイズの新しいメモリ ブロックを割り当て、この新しいメモリ ブロックに渡されるバッファーの内容をコピーします。</span><span class="sxs-lookup"><span data-stu-id="b1636-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="b1636-120">渡されるメモリ ブロックに内部ポインターが含まれている場合、ポインターは新しい場所に合わせて変更されません。</span><span class="sxs-lookup"><span data-stu-id="b1636-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1636-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1636-121">See also</span></span>



[<span data-ttu-id="b1636-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="b1636-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

