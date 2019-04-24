---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357310"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="da583-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="da583-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="da583-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da583-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da583-105">メモリバッファーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="da583-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da583-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="da583-106">Header file:</span></span>  <br/> |<span data-ttu-id="da583-107">mapix</span><span class="sxs-lookup"><span data-stu-id="da583-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="da583-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="da583-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="da583-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="da583-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="da583-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="da583-110">Called by:</span></span>  <br/> |<span data-ttu-id="da583-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="da583-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="da583-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="da583-112">Parameters</span></span>

 <span data-ttu-id="da583-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="da583-113">_cbSize_</span></span>
  
> <span data-ttu-id="da583-114">順番割り当てるバッファーのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="da583-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="da583-115">_lppbuffer_</span><span class="sxs-lookup"><span data-stu-id="da583-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="da583-116">読み上げ返された割り当て済みバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="da583-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da583-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="da583-117">Return value</span></span>

<span data-ttu-id="da583-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="da583-118">S_OK</span></span> 
  
> <span data-ttu-id="da583-119">呼び出しが成功し、要求されたメモリバッファーが返されました。</span><span class="sxs-lookup"><span data-stu-id="da583-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da583-120">解説</span><span class="sxs-lookup"><span data-stu-id="da583-120">Remarks</span></span>

<span data-ttu-id="da583-121">**MAPIAllocateBuffer**呼び出し処理の間、呼び出し側の実装はオペレーティングシステムからメモリブロックを取得します。</span><span class="sxs-lookup"><span data-stu-id="da583-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="da583-122">メモリバッファーは、偶数番号のバイトアドレスに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="da583-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="da583-123">長い整数アクセスがより効率的になるプラットフォームでは、オペレーティングシステムは、バイト数が4の倍数であるアドレスにバッファーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="da583-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="da583-124">[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すと、メモリが不要になったときに、 [MAPIAllocateMore](mapiallocatemore.md)関数とそれにリンクされているすべてのバッファーを呼び出すことによって、 **MAPIAllocateBuffer**によって割り当てられたメモリバッファーを解放します。</span><span class="sxs-lookup"><span data-stu-id="da583-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da583-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="da583-125">See also</span></span>



[<span data-ttu-id="da583-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="da583-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

