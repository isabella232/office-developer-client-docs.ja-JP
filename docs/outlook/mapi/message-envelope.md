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
# <a name="message-envelope"></a><span data-ttu-id="53a58-103">メッセージエンベロープ</span><span class="sxs-lookup"><span data-stu-id="53a58-103">Message Envelope</span></span>

  
  
<span data-ttu-id="53a58-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53a58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53a58-105">RFC 822 ヘッダーは、次のように MAPI プロパティにマップされます。</span><span class="sxs-lookup"><span data-stu-id="53a58-105">RFC 822 headers are mapped to MAPI properties as follows.</span></span> <span data-ttu-id="53a58-106">PR_SENDER_\*は、次の5つのプロパティの省略形です。</span><span class="sxs-lookup"><span data-stu-id="53a58-106">PR_SENDER_\* is an abbreviation for the following 5 properties:</span></span>
  
 <span data-ttu-id="53a58-107">**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-107">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
  
 <span data-ttu-id="53a58-108">**PR_SENDER_ADDRTYPE**([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-108">**PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="53a58-109">**PR_SENDER_EMAIL_ADDRESS**([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-109">**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="53a58-110">**PR_SENDER_SEARCH_KEY**([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-110">**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))</span></span>
  
 <span data-ttu-id="53a58-111">**PR_SENDER_ENTRYID**([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-111">**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="53a58-112">同様の略語は、PR_SENT_REPRESENTING_\*およびその他のメッセージプロパティのグループに使用されます。</span><span class="sxs-lookup"><span data-stu-id="53a58-112">Similar abbreviations are used for PR_SENT_REPRESENTING_\* and other groups of message properties.</span></span>
  
|<span data-ttu-id="53a58-113">**SMTP ヘッダー**</span><span class="sxs-lookup"><span data-stu-id="53a58-113">**SMTP header**</span></span>|<span data-ttu-id="53a58-114">**MAPI プロパティ**</span><span class="sxs-lookup"><span data-stu-id="53a58-114">**MAPI property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53a58-115">差出人：</span><span class="sxs-lookup"><span data-stu-id="53a58-115">From:</span></span>  <br/> |<span data-ttu-id="53a58-116">送信: PR_SENDER_\*;受信: PR_SENDER_\*および PR_SENT_REPRESENTING_\*</span><span class="sxs-lookup"><span data-stu-id="53a58-116">Outbound: PR_SENDER_\*; inbound: PR_SENDER_\* and PR_SENT_REPRESENTING_\*</span></span>  <br/> |
|<span data-ttu-id="53a58-117">状態</span><span class="sxs-lookup"><span data-stu-id="53a58-117">Date:</span></span>  <br/> |<span data-ttu-id="53a58-118">送信: 現在の時刻。受信: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-118">Outbound: current time; inbound: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="53a58-119">宛先：</span><span class="sxs-lookup"><span data-stu-id="53a58-119">To:</span></span>  <br/> |<span data-ttu-id="53a58-120">**PR_DISPLAY_NAME\*\*\*\*PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) が MAPI_TO の受信者の場合は ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) および**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) for recipients where **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) is MAPI_TO</span></span>  <br/> |
|<span data-ttu-id="53a58-121">]</span><span class="sxs-lookup"><span data-stu-id="53a58-121">Cc:</span></span>  <br/> |<span data-ttu-id="53a58-122">**PR_RECIPIENT_TYPE**が MAPI_CC の受信者用の**PR_DISPLAY_NAME**および**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="53a58-122">**PR_DISPLAY_NAME** and **PR_EMAIL_ADDRESS** for recipients where **PR_RECIPIENT_TYPE** is MAPI_CC</span></span>  <br/> |
|<span data-ttu-id="53a58-123">Bcc</span><span class="sxs-lookup"><span data-stu-id="53a58-123">Bcc:</span></span>  <br/> |<span data-ttu-id="53a58-124">**PR_RECIPIENT_TYPE**が MAPI_BCC の受信者用の**PR_DISPLAY_NAME**および**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="53a58-124">**PR_DISPLAY_NAME** and **PR_EMAIL_ADDRESS** for recipients where **PR_RECIPIENT_TYPE** is MAPI_BCC</span></span>  <br/> |
|||
|<span data-ttu-id="53a58-125">時</span><span class="sxs-lookup"><span data-stu-id="53a58-125">Received:</span></span>  <br/> |<span data-ttu-id="53a58-126">対応する MAPI プロパティはありません。ローカルホスト名とコンポーネント名をここに入力します。</span><span class="sxs-lookup"><span data-stu-id="53a58-126">No corresponding MAPI property; put local host name and your component name here</span></span>  <br/> |
|<span data-ttu-id="53a58-127">返信-領収書:</span><span class="sxs-lookup"><span data-stu-id="53a58-127">Return-receipt-to:</span></span>  <br/> |<span data-ttu-id="53a58-128">**PR_REPORT_NAME**([PidTagReportName](pidtagreportname-canonical-property.md)) および**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-128">**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) and **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="53a58-129">返信先:</span><span class="sxs-lookup"><span data-stu-id="53a58-129">Reply-to:</span></span>  <br/> |<span data-ttu-id="53a58-130">**PR_REPLY_RECIPIENT_ENTRIES**([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) および**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-130">**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="53a58-131">件名：</span><span class="sxs-lookup"><span data-stu-id="53a58-131">Subject:</span></span>  <br/> |<span data-ttu-id="53a58-132">**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))特定の長さ制限はありません。</span><span class="sxs-lookup"><span data-stu-id="53a58-132">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) No particular length limitation.</span></span>  <br/> |
|<span data-ttu-id="53a58-133">MIME-バージョン:</span><span class="sxs-lookup"><span data-stu-id="53a58-133">MIME-version:</span></span>  <br/> |<span data-ttu-id="53a58-134">常に "1.0"</span><span class="sxs-lookup"><span data-stu-id="53a58-134">Always "1.0"</span></span>  <br/> |
|||
|<span data-ttu-id="53a58-135">X-ms-chap 添付ファイル:</span><span class="sxs-lookup"><span data-stu-id="53a58-135">X-MS-Attachment:</span></span>  <br/> |<span data-ttu-id="53a58-136">MS Mail SMTP ゲートウェイとの互換性を確保します。</span><span class="sxs-lookup"><span data-stu-id="53a58-136">For compatibility with MS Mail SMTP gateway.</span></span> <span data-ttu-id="53a58-137">_ (ファイル名のサイズ mm-dd-yyy hh: mm_Details 以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53a58-137">_filename size mm-dd-yyy hh:mm_Details below.</span></span>  <br/> |
|||
| <span data-ttu-id="53a58-138">_SMTP メッセージエンベロープ全体_</span><span class="sxs-lookup"><span data-stu-id="53a58-138">_entire SMTP message envelope_</span></span> <br/> |<span data-ttu-id="53a58-139">**PR_TRANSPORT_MESSAGE_HEADERS**([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-139">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="53a58-140">ヘッダー名未定</span><span class="sxs-lookup"><span data-stu-id="53a58-140">header name TBD</span></span>  <br/> |<span data-ttu-id="53a58-141">**PR_SEND_RICH_INFO**([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _ 送信者のみの場合は、TBDheader を使用して、送信者が応答で TNEF コンテンツを解釈できるかどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53a58-141">**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for sender only._The TBDheader should be used to determine whether the sender is capable of interpreting TNEF content in a reply.</span></span>  <br/> |
|<span data-ttu-id="53a58-142">MessageID</span><span class="sxs-lookup"><span data-stu-id="53a58-142">MessageID:</span></span>  <br/> |<span data-ttu-id="53a58-143">**PR_TNEF_CORRELATION_KEY**([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53a58-143">**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="53a58-144">Content-type</span><span class="sxs-lookup"><span data-stu-id="53a58-144">Content-type</span></span>  <br/> |<span data-ttu-id="53a58-145">text/plain またはマルチパート/mixed のどちらかです。</span><span class="sxs-lookup"><span data-stu-id="53a58-145">Either text/plain or multipart/mixed.</span></span> <span data-ttu-id="53a58-146">「メッセージコンテンツ」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="53a58-146">See "Message Content" section.</span></span>  <br/> |
   
<span data-ttu-id="53a58-147">このヘッダーは、スペースで区切られた4つのトークンとして書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="53a58-147">The X-MS-Attachment header is formatted as four tokens, separated by a space:</span></span>
  
 <span data-ttu-id="53a58-148">_名前のサイズの日付時刻_</span><span class="sxs-lookup"><span data-stu-id="53a58-148">_name size date time_</span></span>
  
<span data-ttu-id="53a58-149">最初のトークンは、スペースが埋め込まれている可能性があるファイル名です。このヘッダーは、受信メッセージの右側から解析する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53a58-149">The first token is the filename, which may contain embedded spaces, so this header should be parsed from the right on inbound messages.</span></span> <span data-ttu-id="53a58-150">サイズはバイト単位です。日付の形式は_mm-dd-yyyy で_、時刻は_hh: mm_として設定されます。</span><span class="sxs-lookup"><span data-stu-id="53a58-150">The size is in bytes; the date is formatted as  _mm-dd-yyyy,_ and the time as  _hh:mm._</span></span>
  
> [!NOTE]
> <span data-ttu-id="53a58-151">MessageID は**PR_SEARCH_KEY**にマップされません。これは、SMTP ドメインがメッセージ識別子の形式に固有の要件を持っているため、任意の MAPI メッセージ識別子をエンコードすることができないためです。</span><span class="sxs-lookup"><span data-stu-id="53a58-151">MessageID is not mapped to **PR_SEARCH_KEY** because the SMTP domain has specific requirements on the format of the message identifier which make it impossible to encode an arbitrary MAPI message identifier.</span></span> <span data-ttu-id="53a58-152">代わりに、MessageID は**PR_TNEF_CORRELATION_KEY**にマップされます。</span><span class="sxs-lookup"><span data-stu-id="53a58-152">Instead, MessageID is mapped to **PR_TNEF_CORRELATION_KEY**.</span></span> <span data-ttu-id="53a58-153">このプロパティは、送信メッセージを送信し、受信メッセージを受信するトランスポートによって使用されるトランスポートによって設定されるトランスポート定義のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="53a58-153">This property is a transport-defined property that is set by the transport sending an outbound message and used by a transport receiving an inbound message.</span></span> <span data-ttu-id="53a58-154">詳細については、「 [TNEF 対応のトランスポートプロバイダーを開発する](developing-a-tnef-enabled-transport-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53a58-154">For more information, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span> 
  

