---
title: 送信キュー テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437575"
---
# <a name="outgoing-queue-tables"></a>送信キュー テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信キュー テーブルには、メッセージ ストアのすべての送信メッセージに関する情報が含まれます。 メッセージ ストア プロバイダーは、MAPI スプーラーが使用する送信キュー テーブルを実装します。 メッセージの送受信をサポートしていないストアでは、このテーブルを実装する必要があります。 
  
送信キュー テーブルにアクセスするには、MAPI スプーラーが [IMsgStore::GetOutgoingQueue メソッドを呼び出](imsgstore-getoutgoingqueue.md) します。 
  
メッセージを前処理し、クライアント アプリケーションから送信された順序と同じ順序でトランスポート プロバイダーに送信する必要があります。 MAPI スプーラーは、送信時間の昇順でメッセージ ストアからのメッセージを受け入れするように設計されています。 この要件のため、一部のメッセージが送信キュー テーブルに表示される前に、いくつかの遅延が発生する可能性があります。 
  
メッセージ ストアは、MAPI スプーラーが送信時刻でメッセージを並べ替えできるよう、送信キュー テーブルでの並べ替えを許可するか、既定の並べ替え順序を送信時間を昇順に設定する必要があります。 
  
送信キュー テーブルは、キューの内容が変更された場合に通知を送信する必要があります。
  
次のプロパティは、送信キュー テーブルで必要な列セットを構成します。
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
送信キュー テーブルの使用方法の詳細については、「メッセージ ストア プロバイダーを使用してメッセージを送信 [する」を参照してください](sending-messages-by-using-message-store-providers.md)。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

