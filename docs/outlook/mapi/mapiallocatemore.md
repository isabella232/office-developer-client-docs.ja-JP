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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357317"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="c4aee-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="c4aee-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="c4aee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4aee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4aee-105">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数で以前に割り当てられた別のバッファーにリンクされているメモリバッファーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c4aee-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4aee-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c4aee-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4aee-107">mapix</span><span class="sxs-lookup"><span data-stu-id="c4aee-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="c4aee-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="c4aee-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4aee-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c4aee-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c4aee-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c4aee-110">Called by:</span></span>  <br/> |<span data-ttu-id="c4aee-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="c4aee-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="c4aee-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c4aee-112">Parameters</span></span>

 <span data-ttu-id="c4aee-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="c4aee-113">_cbSize_</span></span>
  
> <span data-ttu-id="c4aee-114">順番割り当てる新しいバッファーのサイズをバイト単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="c4aee-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="c4aee-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="c4aee-115">_lpObject_</span></span>
  
> <span data-ttu-id="c4aee-116">順番**MAPIAllocateBuffer**を使用して割り当てられた既存の MAPI バッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c4aee-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="c4aee-117">_lppbuffer_</span><span class="sxs-lookup"><span data-stu-id="c4aee-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="c4aee-118">読み上げ新しく割り当てられたバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c4aee-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4aee-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="c4aee-119">Return value</span></span>

<span data-ttu-id="c4aee-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4aee-120">S_OK</span></span> 
  
> <span data-ttu-id="c4aee-121">呼び出しが成功し、要求されたメモリへのポインターが返されました。</span><span class="sxs-lookup"><span data-stu-id="c4aee-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4aee-122">解説</span><span class="sxs-lookup"><span data-stu-id="c4aee-122">Remarks</span></span>

<span data-ttu-id="c4aee-123">**MAPIAllocateMore**呼び出し処理の間、呼び出し側の実装はオペレーティングシステムからメモリブロックを取得します。</span><span class="sxs-lookup"><span data-stu-id="c4aee-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="c4aee-124">メモリバッファーは、偶数番号のバイトアドレスに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c4aee-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="c4aee-125">長い整数アクセスがより効率的になるプラットフォームでは、オペレーティングシステムは、バイト数が4の倍数であるアドレスにバッファーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c4aee-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="c4aee-126">**MAPIAllocateMore**で割り当てられたバッファーを解放する唯一の方法は、 _lpObject_パラメーターで指定したバッファーポインターを[MAPIFreeBuffer](mapifreebuffer.md)関数に渡すことです。</span><span class="sxs-lookup"><span data-stu-id="c4aee-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="c4aee-127">[MAPIAllocateBuffer](mapiallocatebuffer.md)および**MAPIAllocateMore**で割り当てられたメモリバッファー間のリンクによって、 **MAPIFreeBuffer**は両方のバッファーを1回の呼び出しで解放できます。</span><span class="sxs-lookup"><span data-stu-id="c4aee-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

