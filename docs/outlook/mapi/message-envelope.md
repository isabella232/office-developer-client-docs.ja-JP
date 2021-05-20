---
title: メッセージ エンベロープ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427193"
---
# <a name="message-envelope"></a><span data-ttu-id="5d712-103">メッセージ エンベロープ</span><span class="sxs-lookup"><span data-stu-id="5d712-103">Message Envelope</span></span>

  
  
<span data-ttu-id="5d712-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d712-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d712-105">RFC 822 ヘッダーは、次のように MAPI プロパティにマップされます。</span><span class="sxs-lookup"><span data-stu-id="5d712-105">RFC 822 headers are mapped to MAPI properties as follows.</span></span> <span data-ttu-id="5d712-106">PR_SENDER_ \* は、次の 5 つのプロパティの省略形です。</span><span class="sxs-lookup"><span data-stu-id="5d712-106">PR_SENDER_\* is an abbreviation for the following 5 properties:</span></span>
  
 <span data-ttu-id="5d712-107">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-107">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
  
 <span data-ttu-id="5d712-108">**PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-108">**PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="5d712-109">**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-109">**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="5d712-110">**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-110">**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))</span></span>
  
 <span data-ttu-id="5d712-111">**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-111">**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="5d712-112">同様の省略形は、メッセージプロパティPR_SENT_REPRESENTING_ \* 他のグループに使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d712-112">Similar abbreviations are used for PR_SENT_REPRESENTING_\* and other groups of message properties.</span></span>
  
|<span data-ttu-id="5d712-113">**SMTP ヘッダー**</span><span class="sxs-lookup"><span data-stu-id="5d712-113">**SMTP header**</span></span>|<span data-ttu-id="5d712-114">**MAPI プロパティ**</span><span class="sxs-lookup"><span data-stu-id="5d712-114">**MAPI property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d712-115">差出人：</span><span class="sxs-lookup"><span data-stu-id="5d712-115">From:</span></span>  <br/> |<span data-ttu-id="5d712-116">送信: PR_SENDER_ \* ; 受信: PR_SENDER_ と \* PR_SENT_REPRESENTING_\*</span><span class="sxs-lookup"><span data-stu-id="5d712-116">Outbound: PR_SENDER_\*; inbound: PR_SENDER_\* and PR_SENT_REPRESENTING_\*</span></span>  <br/> |
|<span data-ttu-id="5d712-117">日付:</span><span class="sxs-lookup"><span data-stu-id="5d712-117">Date:</span></span>  <br/> |<span data-ttu-id="5d712-118">送信: 現在の時刻。受信 **:** PR_MESSAGE_DELIVERY_TIME ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-118">Outbound: current time; inbound: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="5d712-119">宛先：</span><span class="sxs-lookup"><span data-stu-id="5d712-119">To:</span></span>  <br/> |<span data-ttu-id="5d712-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) および **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) は **、PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) が使用されている受信者MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="5d712-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) for recipients where **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) is MAPI_TO</span></span>  <br/> |
|<span data-ttu-id="5d712-121">Cc:</span><span class="sxs-lookup"><span data-stu-id="5d712-121">Cc:</span></span>  <br/> |<span data-ttu-id="5d712-122">**PR_DISPLAY_NAME\*\*\*\*がPR_EMAIL_ADDRESS** 受信者 **のPR_RECIPIENT_TYPEと** MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="5d712-122">**PR_DISPLAY_NAME** and **PR_EMAIL_ADDRESS** for recipients where **PR_RECIPIENT_TYPE** is MAPI_CC</span></span>  <br/> |
|<span data-ttu-id="5d712-123">Bcc:</span><span class="sxs-lookup"><span data-stu-id="5d712-123">Bcc:</span></span>  <br/> |<span data-ttu-id="5d712-124">**PR_DISPLAY_NAME\*\*\*\*がPR_EMAIL_ADDRESS** 受信者 **のPR_RECIPIENT_TYPEと** MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="5d712-124">**PR_DISPLAY_NAME** and **PR_EMAIL_ADDRESS** for recipients where **PR_RECIPIENT_TYPE** is MAPI_BCC</span></span>  <br/> |
|||
|<span data-ttu-id="5d712-125">受信:</span><span class="sxs-lookup"><span data-stu-id="5d712-125">Received:</span></span>  <br/> |<span data-ttu-id="5d712-126">対応する MAPI プロパティはありません。ローカル ホスト名とコンポーネント名をここに置く</span><span class="sxs-lookup"><span data-stu-id="5d712-126">No corresponding MAPI property; put local host name and your component name here</span></span>  <br/> |
|<span data-ttu-id="5d712-127">戻り値の取得:</span><span class="sxs-lookup"><span data-stu-id="5d712-127">Return-receipt-to:</span></span>  <br/> |<span data-ttu-id="5d712-128">**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) **と** PR_REPORT_ENTRYID ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-128">**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) and **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="5d712-129">返信:</span><span class="sxs-lookup"><span data-stu-id="5d712-129">Reply-to:</span></span>  <br/> |<span data-ttu-id="5d712-130">**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) **および** PR_REPLY_RECIPIENT_NAMES ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-130">**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="5d712-131">件名：</span><span class="sxs-lookup"><span data-stu-id="5d712-131">Subject:</span></span>  <br/> |<span data-ttu-id="5d712-132">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) 特に長さ制限はありません。</span><span class="sxs-lookup"><span data-stu-id="5d712-132">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) No particular length limitation.</span></span>  <br/> |
|<span data-ttu-id="5d712-133">MIME バージョン:</span><span class="sxs-lookup"><span data-stu-id="5d712-133">MIME-version:</span></span>  <br/> |<span data-ttu-id="5d712-134">常に "1.0"</span><span class="sxs-lookup"><span data-stu-id="5d712-134">Always "1.0"</span></span>  <br/> |
|||
|<span data-ttu-id="5d712-135">X-MS-Attachment:</span><span class="sxs-lookup"><span data-stu-id="5d712-135">X-MS-Attachment:</span></span>  <br/> |<span data-ttu-id="5d712-136">MS Mail SMTP ゲートウェイとの互換性のために。</span><span class="sxs-lookup"><span data-stu-id="5d712-136">For compatibility with MS Mail SMTP gateway.</span></span> <span data-ttu-id="5d712-137">_filename mm-dd-yyy hh:mm_Detailsします。</span><span class="sxs-lookup"><span data-stu-id="5d712-137">_filename size mm-dd-yyy hh:mm_Details below.</span></span>  <br/> |
|||
| <span data-ttu-id="5d712-138">_SMTP メッセージ エンベロープ全体_</span><span class="sxs-lookup"><span data-stu-id="5d712-138">_entire SMTP message envelope_</span></span> <br/> |<span data-ttu-id="5d712-139">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-139">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="5d712-140">ヘッダー名 TBD</span><span class="sxs-lookup"><span data-stu-id="5d712-140">header name TBD</span></span>  <br/> |<span data-ttu-id="5d712-141">**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for 送信者 only._The TBDheader を使用して、送信者が返信で TNEF コンテンツを解釈できるかどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d712-141">**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for sender only._The TBDheader should be used to determine whether the sender is capable of interpreting TNEF content in a reply.</span></span>  <br/> |
|<span data-ttu-id="5d712-142">MessageID:</span><span class="sxs-lookup"><span data-stu-id="5d712-142">MessageID:</span></span>  <br/> |<span data-ttu-id="5d712-143">**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d712-143">**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="5d712-144">Content-type</span><span class="sxs-lookup"><span data-stu-id="5d712-144">Content-type</span></span>  <br/> |<span data-ttu-id="5d712-145">テキスト/プレーンまたはマルチパート/混合のいずれか。</span><span class="sxs-lookup"><span data-stu-id="5d712-145">Either text/plain or multipart/mixed.</span></span> <span data-ttu-id="5d712-146">「メッセージ コンテンツ」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d712-146">See "Message Content" section.</span></span>  <br/> |
   
<span data-ttu-id="5d712-147">X-MS-Attachment ヘッダーは、スペースで区切られた 4 つのトークンとして書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="5d712-147">The X-MS-Attachment header is formatted as four tokens, separated by a space:</span></span>
  
 <span data-ttu-id="5d712-148">_名前のサイズの日付時刻_</span><span class="sxs-lookup"><span data-stu-id="5d712-148">_name size date time_</span></span>
  
<span data-ttu-id="5d712-149">最初のトークンはファイル名で、埋め込みスペースが含まれている可能性があります。そのため、このヘッダーは受信メッセージの右側から解析する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d712-149">The first token is the filename, which may contain embedded spaces, so this header should be parsed from the right on inbound messages.</span></span> <span data-ttu-id="5d712-150">サイズはバイト単位です。日付は  _mm-dd-yyyy、_ 時刻は  _hh:mm として書式設定されます。_</span><span class="sxs-lookup"><span data-stu-id="5d712-150">The size is in bytes; the date is formatted as  _mm-dd-yyyy,_ and the time as  _hh:mm._</span></span>
  
> [!NOTE]
> <span data-ttu-id="5d712-151">SMTP ドメインには、任意 **の** MAPI メッセージ識別子をエンコードできないメッセージ識別子の形式に関する特定の要件がある場合、MessageID は PR_SEARCH_KEY にマップされません。</span><span class="sxs-lookup"><span data-stu-id="5d712-151">MessageID is not mapped to **PR_SEARCH_KEY** because the SMTP domain has specific requirements on the format of the message identifier which make it impossible to encode an arbitrary MAPI message identifier.</span></span> <span data-ttu-id="5d712-152">その代わりに、MessageID は **次の** PR_TNEF_CORRELATION_KEY。</span><span class="sxs-lookup"><span data-stu-id="5d712-152">Instead, MessageID is mapped to **PR_TNEF_CORRELATION_KEY**.</span></span> <span data-ttu-id="5d712-153">このプロパティは、送信メッセージを送信するトランスポートによって設定され、受信メッセージを受信するトランスポートによって使用されるトランスポート定義のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="5d712-153">This property is a transport-defined property that is set by the transport sending an outbound message and used by a transport receiving an inbound message.</span></span> <span data-ttu-id="5d712-154">詳細については、「Developing [a TNEF-Enabled トランスポート プロバイダー」を参照してください](developing-a-tnef-enabled-transport-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="5d712-154">For more information, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span> 
  

