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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435391"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="027a7-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="027a7-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="027a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="027a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="027a7-105">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数で以前に割り当てられた別のバッファーにリンクされているメモリ バッファーを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="027a7-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="027a7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="027a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="027a7-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="027a7-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="027a7-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="027a7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="027a7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="027a7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="027a7-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="027a7-110">Called by:</span></span>  <br/> |<span data-ttu-id="027a7-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="027a7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="027a7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="027a7-112">Parameters</span></span>

 <span data-ttu-id="027a7-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="027a7-113">_cbSize_</span></span>
  
> <span data-ttu-id="027a7-114">[in]割り当てる新しいバッファーのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="027a7-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="027a7-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="027a7-115">_lpObject_</span></span>
  
> <span data-ttu-id="027a7-116">[in] **MAPIAllocateBuffer** を使用して割り当てられた既存の MAPI バッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="027a7-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="027a7-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="027a7-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="027a7-118">[out]返された、新しく割り当てられたバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="027a7-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="027a7-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="027a7-119">Return value</span></span>

<span data-ttu-id="027a7-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="027a7-120">S_OK</span></span> 
  
> <span data-ttu-id="027a7-121">呼び出しは成功し、要求されたメモリへのポインターを返しました。</span><span class="sxs-lookup"><span data-stu-id="027a7-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="027a7-122">注釈</span><span class="sxs-lookup"><span data-stu-id="027a7-122">Remarks</span></span>

<span data-ttu-id="027a7-123">**MAPIAllocateMore** 呼び出し処理中に、呼び出し元の実装はオペレーティング システムからメモリ ブロックを取得します。</span><span class="sxs-lookup"><span data-stu-id="027a7-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="027a7-124">メモリ バッファーは、番号が付くバイト アドレスに割り当てされます。</span><span class="sxs-lookup"><span data-stu-id="027a7-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="027a7-125">長整数アクセスの方が効率的なプラットフォームでは、オペレーティング システムは、バイト単位のサイズが 4 の倍数であるアドレスにバッファーを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="027a7-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="027a7-126">**MAPIAllocateMore** で割り当てられたバッファーを解放する唯一の方法は _、lpObject_ パラメーターで指定されたバッファー ポインターを [MAPIFreeBuffer](mapifreebuffer.md)関数に渡す方法です。</span><span class="sxs-lookup"><span data-stu-id="027a7-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="027a7-127">[MAPIAllocateBuffer](mapiallocatebuffer.md)と **MAPIAllocateMore** で割り当てられたメモリ バッファー間のリンクにより **、MAPIFreeBuffer** は 1 回の呼び出しで両方のバッファーを解放できます。</span><span class="sxs-lookup"><span data-stu-id="027a7-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

