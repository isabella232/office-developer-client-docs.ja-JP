---
title: メッセージエンベロープ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356925"
---
# <a name="message-envelope"></a>メッセージエンベロープ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
RFC 822 ヘッダーは、次のように MAPI プロパティにマップされます。 PR_SENDER_\*は、次の5つのプロパティの省略形です。
  
 **PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE**([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS**([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY**([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID**([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
同様の略語は、PR_SENT_REPRESENTING_\*およびその他のメッセージプロパティのグループに使用されます。
  
|**SMTP ヘッダー**|**MAPI プロパティ**|
|:-----|:-----|
|差出人：  <br/> |送信: PR_SENDER_\*;受信: PR_SENDER_\*および PR_SENT_REPRESENTING_\*  <br/> |
|状態  <br/> |送信: 現在の時刻。受信: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|宛先：  <br/> |**PR_DISPLAY_NAME****PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) が MAPI_TO の受信者の場合は ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) および**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|]  <br/> |**PR_RECIPIENT_TYPE**が MAPI_CC の受信者用の**PR_DISPLAY_NAME**および**PR_EMAIL_ADDRESS**  <br/> |
|Bcc  <br/> |**PR_RECIPIENT_TYPE**が MAPI_BCC の受信者用の**PR_DISPLAY_NAME**および**PR_EMAIL_ADDRESS**  <br/> |
|||
|時  <br/> |対応する MAPI プロパティはありません。ローカルホスト名とコンポーネント名をここに入力します。  <br/> |
|返信-領収書:  <br/> |**PR_REPORT_NAME**([PidTagReportName](pidtagreportname-canonical-property.md)) および**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|返信先:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES**([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) および**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|件名：  <br/> |**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))特定の長さ制限はありません。  <br/> |
|MIME-バージョン:  <br/> |常に "1.0"  <br/> |
|||
|X-ms-chap 添付ファイル:  <br/> |MS Mail SMTP ゲートウェイとの互換性を確保します。 _ (ファイル名のサイズ mm-dd-yyy hh: mm_Details 以下を参照してください。  <br/> |
|||
| _SMTP メッセージエンベロープ全体_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS**([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|ヘッダー名未定  <br/> |**PR_SEND_RICH_INFO**([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _ 送信者のみの場合は、TBDheader を使用して、送信者が応答で TNEF コンテンツを解釈できるかどうかを判断する必要があります。  <br/> |
|MessageID  <br/> |**PR_TNEF_CORRELATION_KEY**([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |text/plain またはマルチパート/mixed のどちらかです。 「メッセージコンテンツ」セクションを参照してください。  <br/> |
   
このヘッダーは、スペースで区切られた4つのトークンとして書式設定されます。
  
 _名前のサイズの日付時刻_
  
最初のトークンは、スペースが埋め込まれている可能性があるファイル名です。このヘッダーは、受信メッセージの右側から解析する必要があります。 サイズはバイト単位です。日付の形式は_mm-dd-yyyy で_、時刻は_hh: mm_として設定されます。
  
> [!NOTE]
> MessageID は**PR_SEARCH_KEY**にマップされません。これは、SMTP ドメインがメッセージ識別子の形式に固有の要件を持っているため、任意の MAPI メッセージ識別子をエンコードすることができないためです。 代わりに、MessageID は**PR_TNEF_CORRELATION_KEY**にマップされます。 このプロパティは、送信メッセージを送信し、受信メッセージを受信するトランスポートによって使用されるトランスポートによって設定されるトランスポート定義のプロパティです。 詳細については、「 [TNEF 対応のトランスポートプロバイダーを開発する](developing-a-tnef-enabled-transport-provider.md)」を参照してください。 
  

