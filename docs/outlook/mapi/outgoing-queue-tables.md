---
title: 送信キューテーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437575"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="9e254-103">送信キューテーブル</span><span class="sxs-lookup"><span data-stu-id="9e254-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="9e254-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e254-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e254-105">送信キューテーブルには、メッセージストアのすべての送信メッセージに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9e254-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="9e254-106">メッセージストアプロバイダーは、MAPI スプーラーで使用する送信キューテーブルを実装します。</span><span class="sxs-lookup"><span data-stu-id="9e254-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="9e254-107">メッセージの送信または受信をサポートしていないストアは、この表を実装する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9e254-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="9e254-108">送信キューテーブルにアクセスするために、MAPI スプーラーは[IMsgStore:: getoutgoingqueue](imsgstore-getoutgoingqueue.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e254-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="9e254-109">クライアントアプリケーションによって送信された順序でメッセージがプリプロセスされ、トランスポートプロバイダーに送信されるという要件があります。</span><span class="sxs-lookup"><span data-stu-id="9e254-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="9e254-110">MAPI スプーラーは、メッセージストアからのメッセージを送信時の昇順で受信できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="9e254-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="9e254-111">この要件のため、一部のメッセージが送信キューテーブルに表示されるまでに多少の時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="9e254-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="9e254-112">メッセージストアは、MAPI スプーラーが送信時刻でメッセージを並べ替えることができるように、または既定の並べ替え順序が昇順で送信されるように、送信キューテーブルの並べ替えを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e254-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="9e254-113">キューの内容が変更されたときに、送信キューテーブルは通知を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e254-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="9e254-114">次のプロパティは、送信キューテーブルで必要な列セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="9e254-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e254-115">**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9e254-116">**PR_DISPLAY_BCC**([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="9e254-117">**PR_DISPLAY_CC**([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9e254-118">**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="9e254-119">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9e254-120">**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="9e254-121">**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9e254-122">**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="9e254-123">**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9e254-124">**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="9e254-125">**PR_SUBMIT_FLAGS**([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e254-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="9e254-126">送信キューテーブルの使用方法の詳細については、「[メッセージストアプロバイダーを使用してメッセージを送信](sending-messages-by-using-message-store-providers.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e254-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9e254-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e254-127">See also</span></span>



[<span data-ttu-id="9e254-128">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="9e254-128">MAPI Tables</span></span>](mapi-tables.md)

