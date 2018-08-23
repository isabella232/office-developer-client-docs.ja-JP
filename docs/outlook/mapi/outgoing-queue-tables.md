---
title: 送信キュー テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c5f136a0d26b7519bc1b7b3d8f448f5f382767ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591255"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="6e5a8-103">送信キュー テーブル</span><span class="sxs-lookup"><span data-stu-id="6e5a8-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="6e5a8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e5a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e5a8-105">発信のキュー テーブルには、メッセージ ストアのすべての送信メッセージについての情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="6e5a8-106">メッセージ ストア プロバイダーは、MAPI スプーラーを使用するための発信キュー テーブルを実装します。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="6e5a8-107">ストアの送信をサポートしていないか、メッセージの送受信が必要な次の表を実装しません。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="6e5a8-108">発信のキュー テーブルにアクセスするには、MAPI スプーラーは、 [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="6e5a8-109">メッセージのプリプロセスし、クライアント アプリケーションによって送信された同じ順序でトランスポート プロバイダーに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="6e5a8-110">MAPI スプーラーは、送信時刻の昇順にメッセージ ・ ストアからメッセージを受け付けるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="6e5a8-111">この要件のためがありますいくつかの遅延送信キュー テーブルのいくつかのメッセージが表示される前にします。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="6e5a8-112">メッセージ ストアようにするか、送信キューのテーブルで並べ替えをできるように、MAPI スプーラーは送信時点では、メッセージを並べ替えることができますまたは既定の並べ替え順序が昇順での送信時にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="6e5a8-113">発信キューのテーブルは、キューの内容が変更されたときに通知を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="6e5a8-114">次のプロパティは、発信キュー テーブルに設定する必要な列を構成します。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e5a8-115">**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e5a8-116">**PR_DISPLAY_BCC**([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6e5a8-117">**PR_DISPLAY_CC**([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e5a8-118">**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6e5a8-119">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e5a8-120">**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6e5a8-121">**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e5a8-122">**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6e5a8-123">**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e5a8-124">**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6e5a8-125">**PR_SUBMIT_FLAGS**([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e5a8-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="6e5a8-126">発信キュー テーブルの使用方法の詳細については、[メッセージ ストア プロバイダーを使用してメッセージの送信](sending-messages-by-using-message-store-providers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e5a8-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e5a8-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e5a8-127">See also</span></span>



[<span data-ttu-id="6e5a8-128">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="6e5a8-128">MAPI Tables</span></span>](mapi-tables.md)

