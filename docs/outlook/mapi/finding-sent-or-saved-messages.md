---
title: 送信または保存されたメッセージの検索
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
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="4be4f-103">送信または保存されたメッセージの検索</span><span class="sxs-lookup"><span data-stu-id="4be4f-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="4be4f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4be4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4be4f-105">**保存または送信したすべての送信メッセージを検索するには**</span><span class="sxs-lookup"><span data-stu-id="4be4f-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="4be4f-106">[IMsgStore:: compareentryids](imsgstore-compareentryids.md)を呼び出して、送信したメッセージを含むフォルダーと、受信メッセージを含むフォルダーを比較します。</span><span class="sxs-lookup"><span data-stu-id="4be4f-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="4be4f-107">_lpEntryID1_パラメーターを**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) を指すように設定し、 _lpEntryID2_パラメーターを**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) を指すように設定します。</span><span class="sxs-lookup"><span data-stu-id="4be4f-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="4be4f-108">送信されたメッセージを削除した場合や、送信したメッセージのいずれかを別のフォルダーに移動した場合は、この方法が機能しないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="4be4f-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="4be4f-109">受信メッセージを調べている場合、通常はトランスポートプロバイダーによって設定されるプロパティが存在しないことに注意してください。メッセージがトランスポートプロバイダーによって処理されていないことを前提としています。</span><span class="sxs-lookup"><span data-stu-id="4be4f-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="4be4f-110">これらのプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4be4f-110">These properties include:</span></span>
  
- <span data-ttu-id="4be4f-111">**PR_RECEIVED_BY**プロパティ</span><span class="sxs-lookup"><span data-stu-id="4be4f-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="4be4f-112">**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4be4f-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="4be4f-113">**PR_TRANSPORT_MESSAGE_HEADERS**([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4be4f-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="4be4f-114">**PR_MESSAGE_TO_ME**([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4be4f-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="4be4f-115">**PR_MESSAGE_CC_ME**([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4be4f-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="4be4f-116">**PR_MESSAGE_RECIP_ME**([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4be4f-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

