---
title: メッセージ エンベロープ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fd642575a3136eef3193e0bdbe884cf8f54ba337
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571298"
---
# <a name="message-envelope"></a>メッセージ エンベロープ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
RFC 822 ヘッダーは、MAPI プロパティに次のようにマップされます。 PR_SENDER_\*は、次の 5 つのプロパティの省略形。
  
 **PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE**([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS**([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY**([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID**([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
PR_SENT_REPRESENTING_ のような略語が使用されて\*とメッセージのプロパティの他のグループです。
  
|**SMTP ヘッダー**|**MAPI プロパティ**|
|:-----|:-----|
|差出人：  <br/> |送信: PR_SENDER_\*。受信: PR_SENDER_\*と PR_SENT_REPRESENTING_\*  <br/> |
|日付:  <br/> |送信: 現在の時刻です。受信: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|宛先：  <br/> |**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) と**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) MAPI_TO **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) で、受信者の  <br/> |
|[Cc]:  <br/> |**PR_DISPLAY_NAME**と**PR_RECIPIENT_TYPE**が MAPI_CC を受信者の**PR_EMAIL_ADDRESS**  <br/> |
|[Bcc]:  <br/> |**PR_DISPLAY_NAME**と**PR_RECIPIENT_TYPE**が MAPI_BCC を受信者の**PR_EMAIL_ADDRESS**  <br/> |
|||
|受信します。  <br/> |対応する MAPI プロパティはありません。ローカル ホスト名とコンポーネント名をここに挿入します。  <br/> |
|戻り値で受信確認をします。  <br/> |**PR_REPORT_NAME**([PidTagReportName](pidtagreportname-canonical-property.md)) と**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|返信先。  <br/> |**PR_REPLY_RECIPIENT_ENTRIES**([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) と**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|件名：  <br/> |**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))特定の長さの制限はありません。  <br/> |
|MIME のバージョン:  <br/> |「1.0」では常に  <br/> |
|||
|X MS の接続:  <br/> |MS メールの SMTP ゲートウェイとの互換性です。 _filename サイズ yyy-mm-dd hh:mm_Details 以下です。  <br/> |
|||
| _全体の SMTP メッセージのエンベロープ_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS**([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|ヘッダー名未定  <br/> |**PR_SEND_RICH_INFO**([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for 送信者のみ ._The TBDheader は、送信者が応答で TNEF コンテンツを解釈できるかどうかを使用してください。  <br/> |
|メッセージ Id:  <br/> |**PR_TNEF_CORRELATION_KEY**([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |テキスト/形式またはマルチパートまたは混合します。 [メッセージ コンテンツ] セクションを参照してください。  <br/> |
   
X-MS の添付ファイルのヘッダーは、スペースで区切られた 4 つのトークンとしてフォーマットされています。
  
 _名サイズ日付時刻_
  
最初のトークンでは、ファイル名は、上の受信メッセージのこのヘッダーを解析する必要がありますので、埋め込みスペースが含まれている可能性があります。 サイズはバイトです。日付が_年・月・日_と時刻を書式設定_hh:mm_ 。
  
> [!NOTE]
> SMTP ドメインが固有の要件の形式でメッセージの識別子の任意の MAPI メッセージ識別子をエンコードするために不可能になることがあるために、メッセージ Id が**PR_SEARCH_KEY**にマップされていません。 代わりに、メッセージ Id は、 **PR_TNEF_CORRELATION_KEY**にマップされます。 このプロパティは、トランスポート定義のプロパティは、送信メッセージを送信するトランスポートによって設定され、受信メッセージのトランスポートで使用されることです。 詳細については、 [TNEF-Enabled トランスポート プロバイダーの開発](developing-a-tnef-enabled-transport-provider.md)を参照してください。 
  

