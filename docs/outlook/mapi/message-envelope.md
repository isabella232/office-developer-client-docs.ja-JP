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
# <a name="message-envelope"></a><span data-ttu-id="f66ad-103">メッセージ エンベロープ</span><span class="sxs-lookup"><span data-stu-id="f66ad-103">Message Envelope</span></span>

  
  
<span data-ttu-id="f66ad-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f66ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f66ad-105">RFC 822 ヘッダーは、MAPI プロパティに次のようにマップされます。</span><span class="sxs-lookup"><span data-stu-id="f66ad-105">RFC 822 headers are mapped to MAPI properties as follows.</span></span> <span data-ttu-id="f66ad-106">PR_SENDER_\*は、次の 5 つのプロパティの省略形。</span><span class="sxs-lookup"><span data-stu-id="f66ad-106">PR_SENDER_\* is an abbreviation for the following 5 properties:</span></span>
  
 <span data-ttu-id="f66ad-107">**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-107">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
  
 <span data-ttu-id="f66ad-108">**PR_SENDER_ADDRTYPE**([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-108">**PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="f66ad-109">**PR_SENDER_EMAIL_ADDRESS**([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-109">**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="f66ad-110">**PR_SENDER_SEARCH_KEY**([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-110">**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))</span></span>
  
 <span data-ttu-id="f66ad-111">**PR_SENDER_ENTRYID**([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-111">**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="f66ad-112">PR_SENT_REPRESENTING_ のような略語が使用されて\*とメッセージのプロパティの他のグループです。</span><span class="sxs-lookup"><span data-stu-id="f66ad-112">Similar abbreviations are used for PR_SENT_REPRESENTING_\* and other groups of message properties.</span></span>
  
|<span data-ttu-id="f66ad-113">**SMTP ヘッダー**</span><span class="sxs-lookup"><span data-stu-id="f66ad-113">**SMTP header**</span></span>|<span data-ttu-id="f66ad-114">**MAPI プロパティ**</span><span class="sxs-lookup"><span data-stu-id="f66ad-114">**MAPI property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f66ad-115">差出人：</span><span class="sxs-lookup"><span data-stu-id="f66ad-115">From:</span></span>  <br/> |<span data-ttu-id="f66ad-116">送信: PR_SENDER_\*。受信: PR_SENDER_\*と PR_SENT_REPRESENTING_\*</span><span class="sxs-lookup"><span data-stu-id="f66ad-116">Outbound: PR_SENDER_\*; inbound: PR_SENDER_\* and PR_SENT_REPRESENTING_\*</span></span>  <br/> |
|<span data-ttu-id="f66ad-117">日付:</span><span class="sxs-lookup"><span data-stu-id="f66ad-117">Date:</span></span>  <br/> |<span data-ttu-id="f66ad-118">送信: 現在の時刻です。受信: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-118">Outbound: current time; inbound: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f66ad-119">宛先：</span><span class="sxs-lookup"><span data-stu-id="f66ad-119">To:</span></span>  <br/> |<span data-ttu-id="f66ad-120">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) と**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) MAPI_TO **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) で、受信者の</span><span class="sxs-lookup"><span data-stu-id="f66ad-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) for recipients where **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) is MAPI_TO</span></span>  <br/> |
|<span data-ttu-id="f66ad-121">[Cc]:</span><span class="sxs-lookup"><span data-stu-id="f66ad-121">Cc:</span></span>  <br/> |<span data-ttu-id="f66ad-122">**PR_DISPLAY_NAME**と**PR_RECIPIENT_TYPE**が MAPI_CC を受信者の**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f66ad-122">**PR_DISPLAY_NAME** and **PR_EMAIL_ADDRESS** for recipients where **PR_RECIPIENT_TYPE** is MAPI_CC</span></span>  <br/> |
|<span data-ttu-id="f66ad-123">[Bcc]:</span><span class="sxs-lookup"><span data-stu-id="f66ad-123">Bcc:</span></span>  <br/> |<span data-ttu-id="f66ad-124">**PR_DISPLAY_NAME**と**PR_RECIPIENT_TYPE**が MAPI_BCC を受信者の**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f66ad-124">**PR_DISPLAY_NAME** and **PR_EMAIL_ADDRESS** for recipients where **PR_RECIPIENT_TYPE** is MAPI_BCC</span></span>  <br/> |
|||
|<span data-ttu-id="f66ad-125">受信します。</span><span class="sxs-lookup"><span data-stu-id="f66ad-125">Received:</span></span>  <br/> |<span data-ttu-id="f66ad-126">対応する MAPI プロパティはありません。ローカル ホスト名とコンポーネント名をここに挿入します。</span><span class="sxs-lookup"><span data-stu-id="f66ad-126">No corresponding MAPI property; put local host name and your component name here</span></span>  <br/> |
|<span data-ttu-id="f66ad-127">戻り値で受信確認をします。</span><span class="sxs-lookup"><span data-stu-id="f66ad-127">Return-receipt-to:</span></span>  <br/> |<span data-ttu-id="f66ad-128">**PR_REPORT_NAME**([PidTagReportName](pidtagreportname-canonical-property.md)) と**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-128">**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) and **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f66ad-129">返信先。</span><span class="sxs-lookup"><span data-stu-id="f66ad-129">Reply-to:</span></span>  <br/> |<span data-ttu-id="f66ad-130">**PR_REPLY_RECIPIENT_ENTRIES**([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) と**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-130">**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f66ad-131">件名：</span><span class="sxs-lookup"><span data-stu-id="f66ad-131">Subject:</span></span>  <br/> |<span data-ttu-id="f66ad-132">**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))特定の長さの制限はありません。</span><span class="sxs-lookup"><span data-stu-id="f66ad-132">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) No particular length limitation.</span></span>  <br/> |
|<span data-ttu-id="f66ad-133">MIME のバージョン:</span><span class="sxs-lookup"><span data-stu-id="f66ad-133">MIME-version:</span></span>  <br/> |<span data-ttu-id="f66ad-134">「1.0」では常に</span><span class="sxs-lookup"><span data-stu-id="f66ad-134">Always "1.0"</span></span>  <br/> |
|||
|<span data-ttu-id="f66ad-135">X MS の接続:</span><span class="sxs-lookup"><span data-stu-id="f66ad-135">X-MS-Attachment:</span></span>  <br/> |<span data-ttu-id="f66ad-136">MS メールの SMTP ゲートウェイとの互換性です。</span><span class="sxs-lookup"><span data-stu-id="f66ad-136">For compatibility with MS Mail SMTP gateway.</span></span> <span data-ttu-id="f66ad-137">_filename サイズ yyy-mm-dd hh:mm_Details 以下です。</span><span class="sxs-lookup"><span data-stu-id="f66ad-137">_filename size mm-dd-yyy hh:mm_Details below.</span></span>  <br/> |
|||
| <span data-ttu-id="f66ad-138">_全体の SMTP メッセージのエンベロープ_</span><span class="sxs-lookup"><span data-stu-id="f66ad-138">_entire SMTP message envelope_</span></span> <br/> |<span data-ttu-id="f66ad-139">**PR_TRANSPORT_MESSAGE_HEADERS**([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-139">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f66ad-140">ヘッダー名未定</span><span class="sxs-lookup"><span data-stu-id="f66ad-140">header name TBD</span></span>  <br/> |<span data-ttu-id="f66ad-141">**PR_SEND_RICH_INFO**([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for 送信者のみ ._The TBDheader は、送信者が応答で TNEF コンテンツを解釈できるかどうかを使用してください。</span><span class="sxs-lookup"><span data-stu-id="f66ad-141">**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for sender only._The TBDheader should be used to determine whether the sender is capable of interpreting TNEF content in a reply.</span></span>  <br/> |
|<span data-ttu-id="f66ad-142">メッセージ Id:</span><span class="sxs-lookup"><span data-stu-id="f66ad-142">MessageID:</span></span>  <br/> |<span data-ttu-id="f66ad-143">**PR_TNEF_CORRELATION_KEY**([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f66ad-143">**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f66ad-144">Content-type</span><span class="sxs-lookup"><span data-stu-id="f66ad-144">Content-type</span></span>  <br/> |<span data-ttu-id="f66ad-145">テキスト/形式またはマルチパートまたは混合します。</span><span class="sxs-lookup"><span data-stu-id="f66ad-145">Either text/plain or multipart/mixed.</span></span> <span data-ttu-id="f66ad-146">[メッセージ コンテンツ] セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f66ad-146">See "Message Content" section.</span></span>  <br/> |
   
<span data-ttu-id="f66ad-147">X-MS の添付ファイルのヘッダーは、スペースで区切られた 4 つのトークンとしてフォーマットされています。</span><span class="sxs-lookup"><span data-stu-id="f66ad-147">The X-MS-Attachment header is formatted as four tokens, separated by a space:</span></span>
  
 <span data-ttu-id="f66ad-148">_名サイズ日付時刻_</span><span class="sxs-lookup"><span data-stu-id="f66ad-148">_name size date time_</span></span>
  
<span data-ttu-id="f66ad-149">最初のトークンでは、ファイル名は、上の受信メッセージのこのヘッダーを解析する必要がありますので、埋め込みスペースが含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f66ad-149">The first token is the filename, which may contain embedded spaces, so this header should be parsed from the right on inbound messages.</span></span> <span data-ttu-id="f66ad-150">サイズはバイトです。日付が_年・月・日_と時刻を書式設定_hh:mm_ 。</span><span class="sxs-lookup"><span data-stu-id="f66ad-150">The size is in bytes; the date is formatted as  _mm-dd-yyyy,_ and the time as  _hh:mm._</span></span>
  
> [!NOTE]
> <span data-ttu-id="f66ad-151">SMTP ドメインが固有の要件の形式でメッセージの識別子の任意の MAPI メッセージ識別子をエンコードするために不可能になることがあるために、メッセージ Id が**PR_SEARCH_KEY**にマップされていません。</span><span class="sxs-lookup"><span data-stu-id="f66ad-151">MessageID is not mapped to **PR_SEARCH_KEY** because the SMTP domain has specific requirements on the format of the message identifier which make it impossible to encode an arbitrary MAPI message identifier.</span></span> <span data-ttu-id="f66ad-152">代わりに、メッセージ Id は、 **PR_TNEF_CORRELATION_KEY**にマップされます。</span><span class="sxs-lookup"><span data-stu-id="f66ad-152">Instead, MessageID is mapped to **PR_TNEF_CORRELATION_KEY**.</span></span> <span data-ttu-id="f66ad-153">このプロパティは、トランスポート定義のプロパティは、送信メッセージを送信するトランスポートによって設定され、受信メッセージのトランスポートで使用されることです。</span><span class="sxs-lookup"><span data-stu-id="f66ad-153">This property is a transport-defined property that is set by the transport sending an outbound message and used by a transport receiving an inbound message.</span></span> <span data-ttu-id="f66ad-154">詳細については、 [TNEF-Enabled トランスポート プロバイダーの開発](developing-a-tnef-enabled-transport-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f66ad-154">For more information, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span> 
  

