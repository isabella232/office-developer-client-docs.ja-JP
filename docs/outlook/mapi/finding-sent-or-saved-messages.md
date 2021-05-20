---
title: 送信済みまたは保存済みメッセージの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 86373fae2753df66d4456cc0fc00f8b289977650
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437421"
---
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="2f82c-103">送信済みまたは保存済みメッセージの検索</span><span class="sxs-lookup"><span data-stu-id="2f82c-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="2f82c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f82c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2f82c-105">**保存または送信した送信メッセージを検索するには**</span><span class="sxs-lookup"><span data-stu-id="2f82c-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="2f82c-106">[IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md)を呼び出して、送信されたメッセージを含むフォルダーと受信メッセージを含むフォルダーを比較します。</span><span class="sxs-lookup"><span data-stu-id="2f82c-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="2f82c-107">_lpEntryID1_ パラメーターを **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)をポイントし _、lpEntryID2_ パラメーターを **PR_PARENT_ENTRYID** ([PidTagParentEntryId)](pidtagparententryid-canonical-property.md)をポイントするに設定します。</span><span class="sxs-lookup"><span data-stu-id="2f82c-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="2f82c-108">送信後にメッセージを削除するか、送信されたメッセージを別のフォルダーに移動した場合、この戦略は機能しません。</span><span class="sxs-lookup"><span data-stu-id="2f82c-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="2f82c-109">受信メッセージを調べる中で、トランスポート プロバイダーによって通常設定されているプロパティが見つからない場合は、メッセージがトランスポート プロバイダーによって処理されたことがないと仮定できます。</span><span class="sxs-lookup"><span data-stu-id="2f82c-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="2f82c-110">これらのプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2f82c-110">These properties include:</span></span>
  
- <span data-ttu-id="2f82c-111">**PR_RECEIVED_BY** プロパティ</span><span class="sxs-lookup"><span data-stu-id="2f82c-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="2f82c-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f82c-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="2f82c-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f82c-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="2f82c-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f82c-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="2f82c-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f82c-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="2f82c-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f82c-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

