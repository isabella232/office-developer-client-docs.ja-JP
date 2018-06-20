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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8ba00ecc1d9ff1c0b7db63d3e6d667b374245742
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801484"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="4059a-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4059a-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="4059a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4059a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4059a-105">メモリ バッファーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4059a-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4059a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4059a-106">Header file:</span></span>  <br/> |<span data-ttu-id="4059a-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="4059a-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="4059a-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="4059a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4059a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4059a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4059a-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4059a-110">Called by:</span></span>  <br/> |<span data-ttu-id="4059a-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="4059a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="4059a-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="4059a-112">Parameters</span></span>

 <span data-ttu-id="4059a-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="4059a-113">_cbSize_</span></span>
  
> <span data-ttu-id="4059a-114">[in]割り当てられるバッファーのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="4059a-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="4059a-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="4059a-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="4059a-116">[out]返されるバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4059a-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4059a-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4059a-117">Return value</span></span>

<span data-ttu-id="4059a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4059a-118">S_OK</span></span> 
  
> <span data-ttu-id="4059a-119">呼び出しが成功し、要求されたメモリ バッファーが返されます。</span><span class="sxs-lookup"><span data-stu-id="4059a-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4059a-120">備考</span><span class="sxs-lookup"><span data-stu-id="4059a-120">Remarks</span></span>

<span data-ttu-id="4059a-121">**MAPIAllocateBuffer**の中に処理を呼び出す、呼び出し元の実装は、オペレーティング システムからメモリ ブロックを取得します。</span><span class="sxs-lookup"><span data-stu-id="4059a-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="4059a-122">メモリ バッファーは、偶数のバイト アドレスに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="4059a-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="4059a-123">長整数型のアクセスがより効率的なプラットフォームでは、オペレーティング システムは、バイト単位でサイズが 4 の倍数のアドレスにバッファーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4059a-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="4059a-124">[MAPIFreeBuffer](mapifreebuffer.md)関数のリリースを呼び出す、 [MAPIAllocateMore](mapiallocatemore.md)関数とすべてのバッファーを呼び出すことによって、 **MAPIAllocateBuffer**、によって割り当てられたメモリ バッファーにリンクして、メモリが不要になったとき。</span><span class="sxs-lookup"><span data-stu-id="4059a-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4059a-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="4059a-125">See also</span></span>



[<span data-ttu-id="4059a-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4059a-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

