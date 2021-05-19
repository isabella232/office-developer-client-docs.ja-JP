---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410554"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="ab9e0-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ab9e0-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="ab9e0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab9e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab9e0-105">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数または[MAPIAllocateMore](mapiallocatemore.md)関数の呼び出しで割り当てられたメモリ バッファーを解放します。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab9e0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ab9e0-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab9e0-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="ab9e0-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="ab9e0-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ab9e0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ab9e0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ab9e0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ab9e0-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ab9e0-110">Called by:</span></span>  <br/> |<span data-ttu-id="ab9e0-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ab9e0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="ab9e0-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab9e0-112">Parameters</span></span>

 <span data-ttu-id="ab9e0-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="ab9e0-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="ab9e0-114">[in]以前に割り当てられたメモリ バッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="ab9e0-115">lpBuffer パラメーターで  _NULL が渡_ された場合 **、MAPIFreeBuffer は何** もしません。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ab9e0-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="ab9e0-116">Return value</span></span>

<span data-ttu-id="ab9e0-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab9e0-117">S_OK</span></span> 
  
> <span data-ttu-id="ab9e0-118">呼び出しは成功し、要求されたメモリを解放しました。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="ab9e0-119">**MAPIFreeBuffer** は、既に解放されたS_OKまたは **MAPIAllocateBuffer** と **MAPIAllocateMore** でメモリ ブロックが割り当てられていない場合に、この値を返す場合もあります。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab9e0-120">注釈</span><span class="sxs-lookup"><span data-stu-id="ab9e0-120">Remarks</span></span>

<span data-ttu-id="ab9e0-121">通常、クライアント アプリケーションまたはサービス プロバイダーが [MAPIAllocateBuffer](mapiallocatebuffer.md) または [MAPIAllocateMore](mapiallocatemore.md)を呼び出す場合、オペレーティング システムは、複数のレベルのポインターを持つ 1 つ以上の複雑な構造を 1 つの連続したメモリ バッファーに構築します。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="ab9e0-122">MAPI 関数またはメソッドがこのような内容のバッファーを作成すると、クライアントは、バッファーを作成した MAPI 関数によって返されるバッファーへのポインターを **MAPIFreeBuffer** に渡して、バッファーに含まれるすべての構造体を後で解放できます。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="ab9e0-123">サービス プロバイダーが **MAPIFreeBuffer** を使用してメモリ バッファーを解放するには、プロバイダーのサポート オブジェクトで返されるバッファーへのポインターを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="ab9e0-124">特定のバッファーを **解放する MAPIFreeBuffer** の呼び出しは、クライアントまたはプロバイダーがこのバッファーの使用を終了するとすぐに行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="ab9e0-125">MAPI セッションの [最後に IMAPISession::Logoff](imapisession-logoff.md) メソッドを呼び出すだけで、メモリ バッファーは自動的に解放されません。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="ab9e0-126">クライアントまたはサービス プロバイダーは  _、MAPIFreeBuffer_ から正常に戻った後、lpBuffer で渡されたポインターが無効であるという前提で **動作する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="ab9e0-127">**MAPIAllocateBuffer** または **MAPIAllocateMore** または空きメモリ ブロックを介してメッセージング システムによって割り当てられていないメモリ ブロックがポインターによって示されている場合 **、MAPIFreeBuffer** の動作は未定義です。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ab9e0-128">**MAPIFreeBuffer** に null ポインターを渡すと **、MAPIFreeBuffer** は NULL へのポインターを初期化し、最初にテストすることなくクリーンアップ コードで解放できるので、アプリケーションのクリーンアップ コードを簡単かつ小さくできます。</span><span class="sxs-lookup"><span data-stu-id="ab9e0-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab9e0-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab9e0-129">See also</span></span>



[<span data-ttu-id="ab9e0-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="ab9e0-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

