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
# <a name="finding-sent-or-saved-messages"></a>送信済みまたは保存済みメッセージの検索

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **保存または送信した送信メッセージを検索するには**
  
1. [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md)を呼び出して、送信されたメッセージを含むフォルダーと受信メッセージを含むフォルダーを比較します。 
    
2. _lpEntryID1_ パラメーターを **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)をポイントし _、lpEntryID2_ パラメーターを **PR_PARENT_ENTRYID** ([PidTagParentEntryId)](pidtagparententryid-canonical-property.md)をポイントするに設定します。
    
送信後にメッセージを削除するか、送信されたメッセージを別のフォルダーに移動した場合、この戦略は機能しません。 
  
受信メッセージを調べる中で、トランスポート プロバイダーによって通常設定されているプロパティが見つからない場合は、メッセージがトランスポート プロバイダーによって処理されたことがないと仮定できます。 これらのプロパティは次のとおりです。
  
- **PR_RECEIVED_BY** プロパティ 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

