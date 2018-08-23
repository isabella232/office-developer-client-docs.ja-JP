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
# <a name="outgoing-queue-tables"></a>送信キュー テーブル

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
発信のキュー テーブルには、メッセージ ストアのすべての送信メッセージについての情報が含まれています。 メッセージ ストア プロバイダーは、MAPI スプーラーを使用するための発信キュー テーブルを実装します。 ストアの送信をサポートしていないか、メッセージの送受信が必要な次の表を実装しません。 
  
発信のキュー テーブルにアクセスするには、MAPI スプーラーは、 [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)メソッドを呼び出します。 
  
メッセージのプリプロセスし、クライアント アプリケーションによって送信された同じ順序でトランスポート プロバイダーに送信する必要があります。 MAPI スプーラーは、送信時刻の昇順にメッセージ ・ ストアからメッセージを受け付けるように設計されています。 この要件のためがありますいくつかの遅延送信キュー テーブルのいくつかのメッセージが表示される前にします。 
  
メッセージ ストアようにするか、送信キューのテーブルで並べ替えをできるように、MAPI スプーラーは送信時点では、メッセージを並べ替えることができますまたは既定の並べ替え順序が昇順での送信時にする必要があります。 
  
発信キューのテーブルは、キューの内容が変更されたときに通知を送信する必要があります。
  
次のプロパティは、発信キュー テーブルに設定する必要な列を構成します。
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC**([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC**([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS**([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
発信キュー テーブルの使用方法の詳細については、[メッセージ ストア プロバイダーを使用してメッセージの送信](sending-messages-by-using-message-store-providers.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

