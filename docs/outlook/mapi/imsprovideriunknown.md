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
# <a name="imsprovider--iunknown"></a><span data-ttu-id="2e517-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e517-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="2e517-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e517-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e517-105">メッセージ ストア プロバイダー オブジェクトを介してメッセージ ストア プロバイダーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="2e517-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="2e517-106">このメッセージ ストア プロバイダー オブジェクトは、メッセージ ストア プロバイダーの [MSProviderInit](msproviderinit.md) エントリ ポイント関数によってプロバイダー ログオン時に返されます。</span><span class="sxs-lookup"><span data-stu-id="2e517-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="2e517-107">メッセージ ストア プロバイダー オブジェクトは、主にクライアント アプリケーションと MAPI スプーラーによってメッセージ ストアを開く目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e517-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e517-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2e517-108">Header file:</span></span>  <br/> |<span data-ttu-id="2e517-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="2e517-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="2e517-110">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="2e517-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="2e517-111">メッセージ ストア プロバイダーのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="2e517-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="2e517-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="2e517-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="2e517-113">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2e517-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="2e517-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2e517-114">Called by:</span></span>  <br/> |<span data-ttu-id="2e517-115">MAPI と MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="2e517-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="2e517-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="2e517-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2e517-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="2e517-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="2e517-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="2e517-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="2e517-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="2e517-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2e517-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="2e517-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2e517-121">シャットダウン</span><span class="sxs-lookup"><span data-stu-id="2e517-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="2e517-122">メッセージ ストア プロバイダーを順番に閉じます。</span><span class="sxs-lookup"><span data-stu-id="2e517-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="2e517-123">Logon</span><span class="sxs-lookup"><span data-stu-id="2e517-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="2e517-124">メッセージ ストア プロバイダーの 1 つのインスタンスに MAPI をログオンします。</span><span class="sxs-lookup"><span data-stu-id="2e517-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="2e517-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="2e517-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="2e517-126">MAPI スプーラーをメッセージ ストアにログに記録します。</span><span class="sxs-lookup"><span data-stu-id="2e517-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="2e517-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="2e517-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="2e517-128">2 つのメッセージ ストア エントリ識別子を比較して、同じストア オブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="2e517-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e517-129">注釈</span><span class="sxs-lookup"><span data-stu-id="2e517-129">Remarks</span></span>

<span data-ttu-id="2e517-130">MAPI は、ストア プロバイダーによって開くメッセージ ストアの数に関係なく、セッションごとに 1 つのメッセージ ストア プロバイダー オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e517-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="2e517-131">2 つ目の MAPI セッションが開いているストアにログオンすると、MAPI は **MSProviderInit** を 2 回目に呼び出して、そのセッションで使用する新しいメッセージ ストア プロバイダー オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="2e517-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="2e517-132">正しく動作するには、メッセージ ストア プロバイダー オブジェクトに次の情報が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e517-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="2e517-133">この  _プロバイダー オブジェクトを使用_ して開かれたすべてのストアで使用する lpMalloc メモリ割り当てルーチン ポインター。</span><span class="sxs-lookup"><span data-stu-id="2e517-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="2e517-134">_lpfAllocateBuffer_、_ lpfAllocateMore _、_および lpfFreeBuffer_ ルーチン ポインターから [MAPIAllocateBuffer、MAPIAllocateMore、MAPIFreeBuffer](mapiallocatebuffer.md)メモリ割り当て関数を取得します。 [](mapiallocatemore.md) [](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="2e517-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="2e517-135">このプロバイダー オブジェクトを使用して開き、まだ閉じていないすべてのストアのリンクリスト。</span><span class="sxs-lookup"><span data-stu-id="2e517-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e517-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e517-136">See also</span></span>



[<span data-ttu-id="2e517-137">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="2e517-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

