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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412864"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="70dd1-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="70dd1-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="70dd1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70dd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70dd1-105">メッセージストアプロバイダーオブジェクトを使用して、メッセージストアプロバイダーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="70dd1-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="70dd1-106">このメッセージストアプロバイダオブジェクトは、メッセージストアプロバイダーの[msproviderinit](msproviderinit.md) entry point 関数によってプロバイダログオンで返されます。</span><span class="sxs-lookup"><span data-stu-id="70dd1-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="70dd1-107">メッセージストアプロバイダーオブジェクトは、主にクライアントアプリケーションと MAPI スプーラーによって、メッセージストアを開くために使用されます。</span><span class="sxs-lookup"><span data-stu-id="70dd1-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70dd1-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="70dd1-108">Header file:</span></span>  <br/> |<span data-ttu-id="70dd1-109">Mapispi</span><span class="sxs-lookup"><span data-stu-id="70dd1-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="70dd1-110">公開者:</span><span class="sxs-lookup"><span data-stu-id="70dd1-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="70dd1-111">メッセージ ストア プロバイダーのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="70dd1-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="70dd1-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="70dd1-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="70dd1-113">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="70dd1-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="70dd1-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="70dd1-114">Called by:</span></span>  <br/> |<span data-ttu-id="70dd1-115">mapi および mapi スプーラー</span><span class="sxs-lookup"><span data-stu-id="70dd1-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="70dd1-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="70dd1-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="70dd1-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="70dd1-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="70dd1-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="70dd1-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="70dd1-119">lpmsprovider</span><span class="sxs-lookup"><span data-stu-id="70dd1-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="70dd1-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="70dd1-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="70dd1-121">シャットダウン</span><span class="sxs-lookup"><span data-stu-id="70dd1-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="70dd1-122">メッセージストアプロバイダーを整然と閉じます。</span><span class="sxs-lookup"><span data-stu-id="70dd1-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="70dd1-123">Logon</span><span class="sxs-lookup"><span data-stu-id="70dd1-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="70dd1-124">メッセージストアプロバイダーの1つのインスタンスに MAPI を記録します。</span><span class="sxs-lookup"><span data-stu-id="70dd1-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="70dd1-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="70dd1-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="70dd1-126">MAPI スプーラーをメッセージストアに記録します。</span><span class="sxs-lookup"><span data-stu-id="70dd1-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="70dd1-127">comparestoreids</span><span class="sxs-lookup"><span data-stu-id="70dd1-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="70dd1-128">2つのメッセージストアエントリ識別子を比較して、同じ store オブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="70dd1-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70dd1-129">注釈</span><span class="sxs-lookup"><span data-stu-id="70dd1-129">Remarks</span></span>

<span data-ttu-id="70dd1-130">MAPI では、ストアプロバイダーによって開かれるメッセージストアの数に関係なく、セッションごとに1つのメッセージストアプロバイダオブジェクトが使用されます。</span><span class="sxs-lookup"><span data-stu-id="70dd1-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="70dd1-131">2番目の mapi セッションが開いているストアにログオンすると、mapi は**msproviderinit**をもう一度呼び出して、そのセッションで使用する新しいメッセージストアプロバイダオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="70dd1-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="70dd1-132">メッセージストアプロバイダオブジェクトには、正しく動作するために次のものが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="70dd1-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="70dd1-133">このプロバイダーオブジェクトを使用して開かれたすべてのストアが使用する_lpmalloc_メモリ割り当てルーチンポインター。</span><span class="sxs-lookup"><span data-stu-id="70dd1-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="70dd1-134">[MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)のメモリ割り当て関数への_lpfAllocateBuffer_、_ lpfAllocateMore _、および_lpfFreeBuffer_ルーチンポインター。</span><span class="sxs-lookup"><span data-stu-id="70dd1-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="70dd1-135">このプロバイダオブジェクトを使用して開かれているが、まだ閉じていないすべてのストアのリンクリスト。</span><span class="sxs-lookup"><span data-stu-id="70dd1-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70dd1-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="70dd1-136">See also</span></span>



[<span data-ttu-id="70dd1-137">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="70dd1-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

