---
title: 送信済みまたは保存済みメッセージの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 77d7173a6a62a375108f0d8bcffa3b99237417b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588001"
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
    

