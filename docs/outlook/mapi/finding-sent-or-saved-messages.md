---
title: 送信または保存されたメッセージの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6e8b618e477475e8e7f45c266791086af63d8bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800072"
---
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="b8355-103">送信または保存されたメッセージの検索</span><span class="sxs-lookup"><span data-stu-id="b8355-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="b8355-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b8355-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="b8355-105">**保存または送信したすべての送信メッセージを検索するには**</span><span class="sxs-lookup"><span data-stu-id="b8355-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="b8355-106">受信したメッセージを含むフォルダーに送信済みメッセージを含むフォルダーを比較する[IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b8355-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="b8355-107">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) を指すように_lpEntryID1_パラメーターと**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) を指すように_lpEntryID2_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="b8355-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="b8355-108">削除した場合か、メッセージ送信、または、別のフォルダーに送信したメッセージのいずれかに移動した後、この方法は機能しないことに注意します。</span><span class="sxs-lookup"><span data-stu-id="b8355-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="b8355-109">受信メッセージを調べることでは、通常、トランスポート プロバイダーによって設定されているプロパティが欠落しているを確認する場合、は、メッセージがトランスポート プロバイダーによって処理されたことを想定できます。</span><span class="sxs-lookup"><span data-stu-id="b8355-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="b8355-110">これらのプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b8355-110">These properties include:</span></span>
  
- <span data-ttu-id="b8355-111">**PR_RECEIVED_BY**プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8355-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="b8355-112">**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8355-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="b8355-113">**PR_TRANSPORT_MESSAGE_HEADERS**([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8355-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="b8355-114">**PR_MESSAGE_TO_ME**([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8355-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="b8355-115">**PR_MESSAGE_CC_ME**([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8355-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="b8355-116">**PR_MESSAGE_RECIP_ME**([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8355-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

