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
ms.openlocfilehash: 5a2e4f4b248cb8eefd5ee37c0c90d5ef9c0d0cac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565019"
---
# <a name="finding-sent-or-saved-messages"></a>送信または保存されたメッセージの検索

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 **保存または送信したすべての送信メッセージを検索するには**
  
1. 受信したメッセージを含むフォルダーに送信済みメッセージを含むフォルダーを比較する[IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md)を呼び出します。 
    
2. **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) を指すように_lpEntryID1_パラメーターと**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) を指すように_lpEntryID2_パラメーターを設定します。
    
削除した場合か、メッセージ送信、または、別のフォルダーに送信したメッセージのいずれかに移動した後、この方法は機能しないことに注意します。 
  
受信メッセージを調べることでは、通常、トランスポート プロバイダーによって設定されているプロパティが欠落しているを確認する場合、は、メッセージがトランスポート プロバイダーによって処理されたことを想定できます。 これらのプロパティは次のとおりです。
  
- **PR_RECEIVED_BY**プロパティ 
    
- **PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS**([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME**([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME**([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME**([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

