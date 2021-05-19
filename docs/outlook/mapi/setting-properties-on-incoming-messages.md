---
title: 受信メッセージのプロパティの設定
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d7043004799d534f11aa98770e2e323cbdae95a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432696"
---
# <a name="setting-properties-on-incoming-messages"></a>受信メッセージのプロパティの設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI サブシステム内のクライアント アプリケーションでは、受信したメッセージに多数のプロパティが必要です。 トランスポート プロバイダーがメッセージを MAPI に取り込む場合は、必要な情報を含む唯一のプロセスか、少なくとも情報の最適なソースなので、これらのプロパティを設定する必要があります。
  
プロバイダーは、受信メッセージでこれらのプロパティの値を設定してください。
  
|**プロパティ名**|**説明**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |メッセージの件名。  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |テキスト形式のメッセージ テキスト。  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |圧縮された RTF メッセージ テキスト。  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |メッセージが配信された日時。  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |メッセージの発信元の表示名。  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |メッセージの発信元のアドレス帳エントリ。  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |メッセージの発信元のアドレス帳検索キー。  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |送信者のメッセージング クライアントによってメッセージがメッセージング システムに送信された時刻。  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |送信する代理人の名前。  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |送信代理人のアドレス帳エントリ。  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |送信代理人のアドレス帳検索キー。  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |受信する代理人の名前。  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |受信代理人のアドレス帳エントリ。  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |受信代理人のアドレス帳検索キー。  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |委任された受信者の表示名の一覧をセミコロンとスペース ("; ") で区切ります。  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |返信の委任された受信者の一覧。  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |受信者が(グループではなく) "宛先" 受信者として具体的に名前が付けられたかどうかを示します。  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |受信者が (グループではなく) "cc" 受信者として具体的に名前が付けられたかどうかを示します。  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |受信者が"to"、"cc" または "bcc" 受信者 (グループ内ではない) として具体的に名前が付けられたかどうかを示します。  <br/> |
   
明らかなマッピングがないプロバイダーは、プロパティの **PR_SENT_REPRESENTING** グループを **PR_SENDER** グループと同じ値に設定し、PR_RCVD_REPRESENTING グループのプロパティグループを **PR_RECEIVED_BY** グループと同じ値に設定し **、PR_SENDER** グループの値に基づいてPR_REPLY_RECIPIENT グループのプロパティ グループを構築できます。 たとえば **、PR_SENT_REPRESENTING_NAMEと** 同じ値に設定 **PR_SENDER_NAME。**
  
[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)メソッドPR_ENTRYID呼び出すことによって、必要に応じてPR_ENTRYLISTプロパティまたはプロパティを生成できます。   プロパティ **の PR_SEARCH_KEY** グループは、ユーザーに関連付けられた **PR_ADDRTYPE** プロパティ、コロン (:)、およびユーザーに関連付けられている **PR_EMAIL_ADDRESS** プロパティを連結し、結果を大文字に変更することで生成できます。 API Windows **CharUpperBuff** は、この目的で使用する便利な関数です。 このプロセスで必要となるのは、バイナリ数量と比較できる標準の形式のアドレスを作成する方法です。 トランスポート プロバイダーが電子メール アドレスに関して大文字と小文字を区別する場合は、これは必要ありません。 
  

