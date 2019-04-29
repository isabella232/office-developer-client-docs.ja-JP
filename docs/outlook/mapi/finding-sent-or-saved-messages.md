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
# <a name="finding-sent-or-saved-messages"></a>送信または保存されたメッセージの検索

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **保存または送信したすべての送信メッセージを検索するには**
  
1. [IMsgStore:: compareentryids](imsgstore-compareentryids.md)を呼び出して、送信したメッセージを含むフォルダーと、受信メッセージを含むフォルダーを比較します。 
    
2. _lpEntryID1_パラメーターを**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) を指すように設定し、 _lpEntryID2_パラメーターを**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) を指すように設定します。
    
送信されたメッセージを削除した場合や、送信したメッセージのいずれかを別のフォルダーに移動した場合は、この方法が機能しないことに注意してください。 
  
受信メッセージを調べている場合、通常はトランスポートプロバイダーによって設定されるプロパティが存在しないことに注意してください。メッセージがトランスポートプロバイダーによって処理されていないことを前提としています。 これらのプロパティは次のとおりです。
  
- **PR_RECEIVED_BY**プロパティ 
    
- **PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS**([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME**([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME**([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME**([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

