---
title: 受信メッセージのプロパティの設定
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f6233afffd532c420ae170ae45b1bf93d6571865
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803914"
---
# <a name="setting-properties-on-incoming-messages"></a>受信メッセージのプロパティの設定

  
  
**適用されます**: Outlook 
  
MAPI サブシステム内のクライアント アプリケーションは、受信したメッセージのプロパティの数を期待しています。 トランスポート プロバイダーは、MAPI メッセージが表示するとき、にこれらのプロパティを設定して、ためには、必要な情報のみ、プロセスは、情報の最適なソースでは、少なくとも、または後必要があります。
  
プロバイダーは、受信メッセージのすべてのこれらのプロパティの値を設定することをお勧めします。
  
|**プロパティ名**|**説明**|
|:-----|:-----|
|**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |メッセージの件名。  <br/> |
|**PR_BODY**([PidTagBody](pidtagbody-canonical-property.md))  <br/> |テキスト形式のメッセージ テキストです。  <br/> |
|**PR_RTF_COMPRESSED**([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |圧縮された rtf 形式のメッセージ テキストです。  <br/> |
|**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |日付と時刻、メッセージが配信されました。  <br/> |
|**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |メッセージの発信者の表示名です。  <br/> |
|**PR_SENDER_ENTRYID**([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |メッセージの発信者のアドレス帳のエントリです。  <br/> |
|**PR_SENDER_SEARCH_KEY**([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |メッセージの発信者のアドレス帳検索キーです。  <br/> |
|**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |送信者のメッセージング クライアントがメッセージング システムにメッセージが送信された時刻。  <br/> |
|**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |送信するための代表的な代理人の名前です。  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID**([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |送信側の代理人のアドレス帳のエントリです。  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY**([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |送信側の代理人のアドレス帳検索キーです。  <br/> |
|**PR_RCVD_REPRESENTING_NAME**([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |受信用の代表的な代理人の名前です。  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID**([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |受信側の代理人のアドレス帳のエントリです。  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY**([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |受信側の代理人のアドレス帳検索キーです。  <br/> |
|**PR_REPLY_RECIPIENT_NAMES**([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |代理受信者の一覧の表示名、スペース、セミコロンで区切られます (「;」)。  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES**([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |返信の代理受信者のリストです。  <br/> |
|**PR_MESSAGE_TO_ME**([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |受信者が具体的にはという名前ではなくグループ) を受信者として指定します。  <br/> |
|**PR_MESSAGE_CC_ME**([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |受信者はされた (グループ) ではなく"cc"受信者として明示的に指定することを示します。  <br/> |
|**PR_MESSAGE_RECIP_ME**([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |受信者が具体的にはという名前で、「宛先」とすることを示します (グループ) ではなく、[cc] または [bcc] の受信者です。  <br/> |
   
明確なマッピングがないプロバイダーは、 **PR_SENDER**グループ、 **PR_RCVD_REPRESENTING**グループの**PR_RECEIVED_BY と同じ値にプロパティと同じ値に、 **PR_SENT_REPRESENTING**のグループのプロパティを設定することができます。** グループ、および**PR_SENDER**のグループの値に基づいてプロパティの**PR_REPLY_RECIPIENT**グループを作成できます。 たとえば、 **PR_SENT_REPRESENTING_NAME** **PR_SENDER_NAME**と同じ値に設定できます。
  
**PR_ENTRYID**または**PR_ENTRYLIST**のプロパティを生成できます、必要に応じて、 [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)メソッドを呼び出すことによって。 **PR_SEARCH_KEY**グループのプロパティのユーザー、コロン (:)、および、ユーザーに関連付けられている**PR_EMAIL_ADDRESS**プロパティに関連付けられている**PR_ADDRTYPE**プロパティを連結することによって生成される結果を大文字に変更し、. Windows API 関数**CharUpperBuff**は、この目的に使用する便利な機能です。 このプロセスに要求される、バイナリの数値として比較できるアドレスの正規の形式のことです。 これがトランスポート プロバイダーは、電子メール アドレスに対して大文字小文字を区別する場合は必要ないことに注意してください。 
  

