---
title: メッセージ エンベロープ
manager: lindalu
ms.date: 09/14/2021
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: '最終更新日: 2021 年 9 月 9 日'
ms.openlocfilehash: 787460bfbaebc6294f38dea4889cefec373c25a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620444"
---
# <a name="message-envelope"></a>メッセージ エンベロープ

**適用対象**: Outlook 2013 | Outlook 2016
  
RFC 822 ヘッダーは、次のように MAPI プロパティにマップされます。 PR_SENDER_ \* は、次の 5 つのプロパティの省略形です。
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
同様の省略形は、メッセージプロパティPR_SENT_REPRESENTING_ \* 他のグループに使用されます。
  
|**SMTP ヘッダー**|**MAPI プロパティ**|
|:-----|:-----|
|差出人：  <br/> |送信: PR_SENDER_ \* ; 受信: PR_SENDER_ と \* PR_SENT_REPRESENTING_\*  <br/> |
|日付:  <br/> |送信: 現在の時刻。受信 **:** PR_MESSAGE_DELIVERY_TIME ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|宛先：  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) および **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) は **、PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) が使用されている受信者MAPI_TO  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME****がPR_EMAIL_ADDRESS** 受信者 **のPR_RECIPIENT_TYPEと** MAPI_CC  <br/> |
|Bcc:  <br/> |**PR_DISPLAY_NAME****がPR_EMAIL_ADDRESS** 受信者 **のPR_RECIPIENT_TYPEと** MAPI_BCC  <br/> |
|||
|受信:  <br/> |対応する MAPI プロパティはありません。ローカル ホスト名とコンポーネント名をここに置く  <br/> |
|戻り値の取得:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) **と** PR_REPORT_ENTRYID ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|返信:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) **および** PR_REPLY_RECIPIENT_NAMES ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|件名：  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) 特に長さ制限はありません。  <br/> |
|MIME バージョン:  <br/> |常に "1.0"  <br/> |
|||
|X-MS-Attachment:  <br/> |MS Mail SMTP ゲートウェイとの互換性のために。 _filename mm-dd-yyy hh:mm_Detailsします。  <br/> |
|||
| _SMTP メッセージ エンベロープ全体_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|ヘッダー名 TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for 送信者 only._The TBDheader を使用して、送信者が返信で TNEF コンテンツを解釈できるかどうかを判断する必要があります。  <br/> |
|MessageID:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |テキスト/プレーンまたはマルチパート/混合のいずれか。 「メッセージ コンテンツ」セクションを参照してください。  <br/> |
   
X-MS-Attachment ヘッダーは、スペースで区切られた 4 つのトークンとして書式設定されます。
  
 _名前のサイズの日付時刻_
  
最初のトークンはファイル名で、埋め込みスペースが含まれている可能性があります。そのため、このヘッダーは受信メッセージの右側から解析する必要があります。 サイズはバイト単位です。日付は  _mm-dd-yyyy、_ 時刻は  _hh:mm として書式設定されます。_
  
> [!NOTE]
> SMTP ドメインには、任意 **の** MAPI メッセージ識別子をエンコードできないメッセージ識別子の形式に関する特定の要件がある場合、MessageID は PR_SEARCH_KEY にマップされません。 その代わりに、MessageID は **次の** PR_TNEF_CORRELATION_KEY。 このプロパティは、送信メッセージを送信するトランスポートによって設定され、受信メッセージを受信するトランスポートによって使用されるトランスポート定義のプロパティです。 詳細については、「Developing [a TNEF-Enabled トランスポート プロバイダー」を参照してください](developing-a-tnef-enabled-transport-provider.md)。
