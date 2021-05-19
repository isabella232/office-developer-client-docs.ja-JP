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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425695"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="442e4-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="442e4-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="442e4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="442e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="442e4-105">メモリ バッファーを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="442e4-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="442e4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="442e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="442e4-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="442e4-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="442e4-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="442e4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="442e4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="442e4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="442e4-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="442e4-110">Called by:</span></span>  <br/> |<span data-ttu-id="442e4-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="442e4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="442e4-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="442e4-112">Parameters</span></span>

 <span data-ttu-id="442e4-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="442e4-113">_cbSize_</span></span>
  
> <span data-ttu-id="442e4-114">[in]割り当てるバッファーのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="442e4-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="442e4-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="442e4-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="442e4-116">[out]返された割り当てられたバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="442e4-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="442e4-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="442e4-117">Return value</span></span>

<span data-ttu-id="442e4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="442e4-118">S_OK</span></span> 
  
> <span data-ttu-id="442e4-119">呼び出しが成功し、要求されたメモリ バッファーが返されました。</span><span class="sxs-lookup"><span data-stu-id="442e4-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="442e4-120">注釈</span><span class="sxs-lookup"><span data-stu-id="442e4-120">Remarks</span></span>

<span data-ttu-id="442e4-121">**MAPIAllocateBuffer 呼び出し処理** 中に、呼び出し元の実装はオペレーティング システムからメモリ ブロックを取得します。</span><span class="sxs-lookup"><span data-stu-id="442e4-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="442e4-122">メモリ バッファーは、番号が付くバイト アドレスに割り当てされます。</span><span class="sxs-lookup"><span data-stu-id="442e4-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="442e4-123">長整数アクセスの方が効率的なプラットフォームでは、オペレーティング システムは、バイト単位のサイズが 4 の倍数であるアドレスにバッファーを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="442e4-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="442e4-124">[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって **、MAPIAllocateBuffer** によって割り当てられたメモリ バッファーが解放されます [。MAPIAllocateMore](mapiallocatemore.md)関数と、その関数にリンクされているバッファーは、メモリが不要になったときに呼び出します。</span><span class="sxs-lookup"><span data-stu-id="442e4-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="442e4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="442e4-125">See also</span></span>



[<span data-ttu-id="442e4-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="442e4-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

