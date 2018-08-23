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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 22aad12010a4f367e18443d8c0831c6262cc37fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801521"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="e08f8-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e08f8-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="e08f8-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e08f8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e08f8-105">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数または[MAPIAllocateMore](mapiallocatemore.md)関数の呼び出しで割り当てられたメモリ バッファーを解放します。</span><span class="sxs-lookup"><span data-stu-id="e08f8-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e08f8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e08f8-106">Header file:</span></span>  <br/> |<span data-ttu-id="e08f8-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="e08f8-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="e08f8-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e08f8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e08f8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e08f8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e08f8-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e08f8-110">Called by:</span></span>  <br/> |<span data-ttu-id="e08f8-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e08f8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="e08f8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e08f8-112">Parameters</span></span>

 <span data-ttu-id="e08f8-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="e08f8-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="e08f8-114">[in]以前に割り当てられたメモリ バッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e08f8-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="e08f8-115">_LpBuffer_パラメーターに NULL を渡した場合は、 **MAPIFreeBuffer**は何もしません。</span><span class="sxs-lookup"><span data-stu-id="e08f8-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e08f8-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e08f8-116">Return value</span></span>

<span data-ttu-id="e08f8-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="e08f8-117">S_OK</span></span> 
  
> <span data-ttu-id="e08f8-118">呼び出しが成功し、要求されたメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="e08f8-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="e08f8-119">**MAPIFreeBuffer**では、既に解放された場所または**MAPIAllocateBuffer**と**MAPIAllocateMore**を持つメモリ ブロックが割り当てられていないかどうかに S_OK を返すこともします。</span><span class="sxs-lookup"><span data-stu-id="e08f8-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e08f8-120">注釈</span><span class="sxs-lookup"><span data-stu-id="e08f8-120">Remarks</span></span>

<span data-ttu-id="e08f8-121">通常、クライアント アプリケーションまたはサービス プロバイダーを呼び出すと[MAPIAllocateBuffer](mapiallocatebuffer.md)または[MAPIAllocateMore](mapiallocatemore.md)、1 つの連続するメモリ バッファーにオペレーティング システムの構成要素のポインターの複数のレベルの 1 つまたは複数の複雑な構造です。</span><span class="sxs-lookup"><span data-stu-id="e08f8-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="e08f8-122">MAPI の関数またはメソッドは、このような内容でバッファーを作成するとき、クライアントは後で**MAPIFreeBuffer**にバッファーを作成した MAPI 関数から返されるバッファーへのポインターを渡すことによって、バッファーに含まれるすべての構造体を解放できます。</span><span class="sxs-lookup"><span data-stu-id="e08f8-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="e08f8-123">サービス プロバイダーが**MAPIFreeBuffer**を使用してメモリ バッファーを解放するには、プロバイダーのサポート オブジェクトが返されるバッファーへのポインターを渡す必要があること。</span><span class="sxs-lookup"><span data-stu-id="e08f8-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="e08f8-124">特定のバッファーを解放するのには、 **MAPIFreeBuffer**への呼び出しは、クライアントとすぐに行う必要があります。 またはプロバイダーは、このバッファーの使用を終了します。</span><span class="sxs-lookup"><span data-stu-id="e08f8-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="e08f8-125">MAPI セッションの最後に[IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出すだけでも、メモリ バッファーは自動的に解放されません。</span><span class="sxs-lookup"><span data-stu-id="e08f8-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="e08f8-126">クライアントまたはサービス プロバイダーは、 _lpBuffer_で、渡されたポインターが無効である**MAPIFreeBuffer**から正常に戻った後を前提として動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08f8-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="e08f8-127">ポインターには、 **MAPIAllocateBuffer**または**MAPIAllocateMore**またはメモリの空きブロックを使用してメッセージング システムによって割り当てられなかったメモリ ブロックが示されている場合の**MAPIFreeBuffer**の動作は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="e08f8-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e08f8-128">**MAPIFreeBuffer**に null ポインターを渡すことにより、アプリケーションのクリーンアップ コードより単純で小さな**MAPIFreeBuffer**が NULL へのポインターを初期化し、それらを最初にテストすることがなくクリーンアップ コードで解放するためです。</span><span class="sxs-lookup"><span data-stu-id="e08f8-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e08f8-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e08f8-129">See also</span></span>



[<span data-ttu-id="e08f8-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="e08f8-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

