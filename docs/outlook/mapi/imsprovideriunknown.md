---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9444806347c97077b03922b116e2ed7f61665cc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801054"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="7c82f-103">IMSProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c82f-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="7c82f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c82f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c82f-105">メッセージ ストア プロバイダー オブジェクトを使用して、メッセージ ストア プロバイダーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="7c82f-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="7c82f-106">このメッセージ ストア プロバイダー オブジェクトは、メッセージ ストア プロバイダーの[MSProviderInit](msproviderinit.md)のエントリ ポイント関数がプロバイダーへのログオンに返されます。</span><span class="sxs-lookup"><span data-stu-id="7c82f-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="7c82f-107">メッセージ ストア プロバイダー オブジェクトは、メッセージ ストアを開くクライアント アプリケーションと MAPI スプーラーによって主に使用します。</span><span class="sxs-lookup"><span data-stu-id="7c82f-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c82f-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7c82f-108">Header file:</span></span>  <br/> |<span data-ttu-id="7c82f-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="7c82f-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="7c82f-110">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="7c82f-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="7c82f-111">メッセージ ストア プロバイダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7c82f-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="7c82f-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="7c82f-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="7c82f-113">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7c82f-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="7c82f-114">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7c82f-114">Called by:</span></span>  <br/> |<span data-ttu-id="7c82f-115">MAPI および MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="7c82f-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="7c82f-116">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="7c82f-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7c82f-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="7c82f-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="7c82f-118">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="7c82f-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="7c82f-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="7c82f-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7c82f-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="7c82f-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7c82f-121">シャット ダウン</span><span class="sxs-lookup"><span data-stu-id="7c82f-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="7c82f-122">適切な順序で、メッセージ ストア プロバイダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7c82f-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="7c82f-123">Logon</span><span class="sxs-lookup"><span data-stu-id="7c82f-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="7c82f-124">MAPI メッセージ ストア プロバイダーのインスタンスを 1 つにログに記録します。</span><span class="sxs-lookup"><span data-stu-id="7c82f-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="7c82f-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="7c82f-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="7c82f-126">メッセージ ストアに、MAPI スプーラーをログに記録します。</span><span class="sxs-lookup"><span data-stu-id="7c82f-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="7c82f-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="7c82f-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="7c82f-128">比較 2 つのメッセージが同じストア オブジェクトを参照しているかどうかを判断するのには、ストア エントリ id です。</span><span class="sxs-lookup"><span data-stu-id="7c82f-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c82f-129">備考</span><span class="sxs-lookup"><span data-stu-id="7c82f-129">Remarks</span></span>

<span data-ttu-id="7c82f-130">MAPI セッションごとに 1 つのメッセージ ストア プロバイダー オブジェクトを使用して、メッセージの数に関係なく、ストアがストア プロバイダーによって開かれています。</span><span class="sxs-lookup"><span data-stu-id="7c82f-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="7c82f-131">2 つ目 MAPI セッションが開いているすべての店舗に場合、MAPI 呼び出し**MSProviderInit** 2 回目を使用するには、そのセッション用の新しいメッセージ ストア プロバイダー オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="7c82f-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="7c82f-132">メッセージ ストア プロバイダー オブジェクトは、正常に動作させるのには、次を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c82f-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="7c82f-133">_LpMalloc_メモリ割り当てルーチンのポインターこのプロバイダー オブジェクトを使用して開かれたすべての店舗で使用するため。</span><span class="sxs-lookup"><span data-stu-id="7c82f-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="7c82f-134">_LpfAllocateBuffer_、_ lpfAllocateMore _ と_lpfFreeBuffer_ルーチンへのポインター、 [MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)のメモリ割り当て関数。</span><span class="sxs-lookup"><span data-stu-id="7c82f-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="7c82f-135">このプロバイダー オブジェクトを使用して開かれ、閉じられていないすべてのストアのリンクのリストです。</span><span class="sxs-lookup"><span data-stu-id="7c82f-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c82f-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c82f-136">See also</span></span>



[<span data-ttu-id="7c82f-137">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7c82f-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

