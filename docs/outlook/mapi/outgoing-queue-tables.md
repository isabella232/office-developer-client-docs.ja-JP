---
title: 送信キューテーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348504"
---
# <a name="outgoing-queue-tables"></a>送信キューテーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信キューテーブルには、メッセージストアのすべての送信メッセージに関する情報が含まれています。 メッセージストアプロバイダーは、MAPI スプーラーで使用する送信キューテーブルを実装します。 メッセージの送信または受信をサポートしていないストアは、この表を実装する必要はありません。 
  
送信キューテーブルにアクセスするために、MAPI スプーラーは[IMsgStore:: getoutgoingqueue](imsgstore-getoutgoingqueue.md)メソッドを呼び出します。 
  
クライアントアプリケーションによって送信された順序でメッセージがプリプロセスされ、トランスポートプロバイダーに送信されるという要件があります。 MAPI スプーラーは、メッセージストアからのメッセージを送信時の昇順で受信できるように設計されています。 この要件のため、一部のメッセージが送信キューテーブルに表示されるまでに多少の時間がかかることがあります。 
  
メッセージストアは、MAPI スプーラーが送信時刻でメッセージを並べ替えることができるように、または既定の並べ替え順序が昇順で送信されるように、送信キューテーブルの並べ替えを許可する必要があります。 
  
キューの内容が変更されたときに、送信キューテーブルは通知を送信する必要があります。
  
次のプロパティは、送信キューテーブルで必要な列セットを作成します。
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC**([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC**([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS**([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
送信キューテーブルの使用方法の詳細については、「[メッセージストアプロバイダーを使用してメッセージを送信](sending-messages-by-using-message-store-providers.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

