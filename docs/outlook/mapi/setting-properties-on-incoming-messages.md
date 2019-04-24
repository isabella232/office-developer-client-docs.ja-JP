---
title: 受信メッセージに対するプロパティの設定
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d7043004799d534f11aa98770e2e323cbdae95a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339362"
---
# <a name="setting-properties-on-incoming-messages"></a>受信メッセージに対するプロパティの設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI サブシステム内のクライアントアプリケーションは、受信したメッセージに多数のプロパティを想定しています。 トランスポートプロバイダーは、メッセージを MAPI に取り込むときに、これらのプロパティを設定する必要があります。これは、必要な情報が含まれている唯一のプロセスであるか、または少なくとも情報の最適なソースであるからです。
  
プロバイダーは、受信メッセージのすべてのプロパティの値を設定することをお勧めします。
  
|**プロパティ名**|**説明**|
|:-----|:-----|
|**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |メッセージの件名。  <br/> |
|**PR_BODY**([PidTagBody](pidtagbody-canonical-property.md))  <br/> |テキスト形式のメッセージテキスト。  <br/> |
|**PR_RTF_COMPRESSED**([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |圧縮された RTF メッセージテキスト。  <br/> |
|**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |メッセージが配信された日付と時刻。  <br/> |
|**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |メッセージ発信者の表示名。  <br/> |
|**PR_SENDER_ENTRYID**([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |メッセージ発信者のアドレス帳のエントリ。  <br/> |
|**PR_SENDER_SEARCH_KEY**([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |メッセージ発信者のアドレス帳検索キー。  <br/> |
|**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |送信者のメッセージングクライアントによってメッセージがメッセージングシステムに送信された時刻。  <br/> |
|**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |送信する代理人の代理人の名前を指定します。  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID**([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |送信側の代理人のアドレス帳のエントリ。  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY**([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |送信側の代理人のアドレス帳検索キー。  <br/> |
|**PR_RCVD_REPRESENTING_NAME**([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |受信者の代理人の名前を指定します。  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID**([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |受信側の代理人のアドレス帳のエントリ。  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY**([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |受信側の代理人のアドレス帳検索キー。  <br/> |
|**PR_REPLY_RECIPIENT_NAMES**([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |委任された受信者の表示名のリスト。セミコロンとスペース (";") で区切ります。  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES**([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |返信の委任された受信者のリスト。  <br/> |
|**PR_MESSAGE_TO_ME**([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |受信者が明示的に "宛先" 受信者として指定された (グループにはない) ことを示します。  <br/> |
|**PR_MESSAGE_CC_ME**([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |受信者が明示的に "cc" 受信者として指定された (グループにはない) ことを示します。  <br/> |
|**PR_MESSAGE_RECIP_ME**([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |受信者が具体的に "宛先"、"cc"、または "bcc" 受信者として指定された (グループにはない) ことを示します。  <br/> |
   
明白なマッピングを持たないプロバイダーは、プロパティの**PR_SENT_REPRESENTING**グループを**PR_SENDER**グループと同じ値に設定できます。プロパティの**PR_RCVD_REPRESENTING**グループは、PR_RECEIVED_BY と同じ値に設定できます。 **** **PR_SENDER**グループの値に基づいて、プロパティの**PR_REPLY_RECIPIENT**グループを作成できます。 たとえば、 **PR_SENT_REPRESENTING_NAME**を**PR_SENDER_NAME**と同じ値に設定できます。
  
**PR_ENTRYID**または**PR_ENTRYLIST**プロパティは、必要に応じて、 [imapisupport:: createoneoff](imapisupport-createoneoff.md)メソッドを呼び出すことによって生成できます。 プロパティの**PR_SEARCH_KEY**グループは、ユーザーに関連付けられている**PR_ADDRTYPE**プロパティ、コロン (:)、およびユーザーに関連付けられている**PR_EMAIL_ADDRESS**プロパティを連結することによって生成できます。その後、結果を大文字に変更します。. Windows API 関数**CharUpperBuff**は、この目的に使用する便利な関数です。 このプロセスで必要となるのは、2進数量として比較できる標準的な形式のアドレスを作成することです。 これは、トランスポートプロバイダーが電子メールアドレスに関して大文字と小文字を区別する場合には必要ありません。 
  

