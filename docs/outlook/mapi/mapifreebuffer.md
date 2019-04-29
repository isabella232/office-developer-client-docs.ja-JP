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
# <a name="mapifreebuffer"></a><span data-ttu-id="115e6-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="115e6-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="115e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="115e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="115e6-105">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数または[MAPIAllocateMore](mapiallocatemore.md)関数の呼び出しで割り当てられたメモリバッファーを解放します。</span><span class="sxs-lookup"><span data-stu-id="115e6-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="115e6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="115e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="115e6-107">mapix</span><span class="sxs-lookup"><span data-stu-id="115e6-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="115e6-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="115e6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="115e6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="115e6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="115e6-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="115e6-110">Called by:</span></span>  <br/> |<span data-ttu-id="115e6-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="115e6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="115e6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="115e6-112">Parameters</span></span>

 <span data-ttu-id="115e6-113">_lpbuffer_</span><span class="sxs-lookup"><span data-stu-id="115e6-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="115e6-114">順番以前に割り当てられたメモリバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="115e6-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="115e6-115">_lpbuffer_パラメーターで NULL が渡された場合、 **MAPIFreeBuffer**は何も実行しません。</span><span class="sxs-lookup"><span data-stu-id="115e6-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="115e6-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="115e6-116">Return value</span></span>

<span data-ttu-id="115e6-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="115e6-117">S_OK</span></span> 
  
> <span data-ttu-id="115e6-118">呼び出しが成功し、要求されたメモリが解放されました。</span><span class="sxs-lookup"><span data-stu-id="115e6-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="115e6-119">**MAPIFreeBuffer**は、既に解放されている場所にある S_OK を返すことも、 **MAPIAllocateBuffer**および**MAPIAllocateMore**を使用してメモリブロックが割り当てられていない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="115e6-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="115e6-120">注釈</span><span class="sxs-lookup"><span data-stu-id="115e6-120">Remarks</span></span>

<span data-ttu-id="115e6-121">通常、クライアントアプリケーションまたはサービスプロバイダーが[MAPIAllocateBuffer](mapiallocatebuffer.md)または[MAPIAllocateMore](mapiallocatemore.md)を呼び出す場合、オペレーティングシステムは、複数のポインターレベルを持つ1つまたは複数の複雑な構造体に1つ以上の連続したメモリバッファーを構築します。</span><span class="sxs-lookup"><span data-stu-id="115e6-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="115e6-122">mapi 関数またはメソッドがこのような内容のバッファーを作成すると、クライアントは後でバッファーに格納されているすべての構造を解放して、バッファーを作成した mapi 関数によって返されるバッファーへのポインターを**MAPIFreeBuffer**に渡します。</span><span class="sxs-lookup"><span data-stu-id="115e6-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="115e6-123">**MAPIFreeBuffer**を使用してメモリバッファーを解放するサービスプロバイダーの場合は、プロバイダーのサポートオブジェクトで返されるバッファーにポインターを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="115e6-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="115e6-124">**MAPIFreeBuffer**の呼び出しは、クライアントまたはプロバイダーがこのバッファーを使用して終了した直後に、特定のバッファーを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="115e6-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="115e6-125">MAPI セッションの終了時に[imapisession:: Logoff](imapisession-logoff.md)メソッドを呼び出すだけでは、メモリバッファーは自動的には解放されません。</span><span class="sxs-lookup"><span data-stu-id="115e6-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="115e6-126">クライアントまたはサービスプロバイダーは、 **MAPIFreeBuffer**から正常に復帰した後、 _lpbuffer_で渡されたポインターが無効であることを前提として動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="115e6-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="115e6-127">**MAPIAllocateBuffer**または**MAPIAllocateMore**を介して、メッセージングシステムによって割り当てられていないメモリブロックまたは空きメモリブロックのいずれかがポインターに示されている場合、 **MAPIFreeBuffer**の動作は未定義です。</span><span class="sxs-lookup"><span data-stu-id="115e6-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="115e6-128">**MAPIFreeBuffer**に null ポインターを渡すと、 **MAPIFreeBuffer**はポインターを null に初期化し、それを最初にテストしなくても、ポインターを null に初期化し、クリーンアップコード内でそれらを解放できるため、アプリケーションのクリーンアップコードがより簡単になります。</span><span class="sxs-lookup"><span data-stu-id="115e6-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="115e6-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="115e6-129">See also</span></span>



[<span data-ttu-id="115e6-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="115e6-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

