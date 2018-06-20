---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801497"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="1b458-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="1b458-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="1b458-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b458-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b458-105">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数で割り当てられている別のバッファーにリンクされているメモリ バッファーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="1b458-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b458-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1b458-106">Header file:</span></span>  <br/> |<span data-ttu-id="1b458-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="1b458-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="1b458-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="1b458-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1b458-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1b458-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1b458-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1b458-110">Called by:</span></span>  <br/> |<span data-ttu-id="1b458-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1b458-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="1b458-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="1b458-112">Parameters</span></span>

 <span data-ttu-id="1b458-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="1b458-113">_cbSize_</span></span>
  
> <span data-ttu-id="1b458-114">[in]割り当てられる新しいバッファーのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="1b458-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="1b458-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="1b458-115">_lpObject_</span></span>
  
> <span data-ttu-id="1b458-116">[in]**MAPIAllocateBuffer**を使用して割り当てられている既存の MAPI バッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b458-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="1b458-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="1b458-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="1b458-118">[out]返されるへのポインターでは、バッファーが新しく割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1b458-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b458-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1b458-119">Return value</span></span>

<span data-ttu-id="1b458-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b458-120">S_OK</span></span> 
  
> <span data-ttu-id="1b458-121">呼び出しが成功し、要求されたメモリへのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="1b458-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b458-122">備考</span><span class="sxs-lookup"><span data-stu-id="1b458-122">Remarks</span></span>

<span data-ttu-id="1b458-123">**MAPIAllocateMore**の中に処理を呼び出す、呼び出し元の実装は、オペレーティング システムからメモリ ブロックを取得します。</span><span class="sxs-lookup"><span data-stu-id="1b458-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="1b458-124">メモリ バッファーは、偶数のバイト アドレスに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1b458-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="1b458-125">長整数型のアクセスがより効率的なプラットフォームでは、オペレーティング システムは、バイト単位でサイズが 4 の倍数のアドレスにバッファーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="1b458-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="1b458-126">**MAPIAllocateMore**で割り当てられたバッファーを解放する唯一の方法では、 [MAPIFreeBuffer](mapifreebuffer.md)関数に_lpObject_パラメーターで指定されたバッファーのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="1b458-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="1b458-127">[MAPIAllocateBuffer](mapiallocatebuffer.md)と**MAPIAllocateMore**で割り当てられたメモリ バッファーの間のリンクは、1 回の呼び出しの両方のバッファーを解放する**MAPIFreeBuffer**を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1b458-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

