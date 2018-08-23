---
title: メッセージを転送
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 146c8b4d711982118fd9da185a5b095a1bae6b2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800113"
---
# <a name="forwarding-a-message"></a><span data-ttu-id="13c0e-103">メッセージを転送</span><span class="sxs-lookup"><span data-stu-id="13c0e-103">Forwarding a message</span></span>

<span data-ttu-id="13c0e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13c0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13c0e-105">元のメッセージを送信すると同じタスクの多くは、メッセージを転送します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-105">Forwarding a message involves many of the same tasks as sending an original message.</span></span> <span data-ttu-id="13c0e-106">まず、既定のメッセージ ストアと、送信トレイでは通常、送信されるメッセージを保持するために指定されているフォルダーを開くしを転送するメッセージを作成するのには、このフォルダーの[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="13c0e-106">First, you must open the default message store and the folder that is designated to hold outgoing messages, typically the Outbox, and call this folder's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message to be forwarded.</span></span> <span data-ttu-id="13c0e-107">受信トレイでは通常、元のメッセージを保持しているフォルダーを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="13c0e-107">You must also open the folder that holds the original message, typically the Inbox.</span></span> <span data-ttu-id="13c0e-108">別のフォルダーを開く方法については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13c0e-108">For information about opening different folders, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
  
<span data-ttu-id="13c0e-109">転送するメッセージを作成し、元の作成の主な違いでは、転送されたメッセージを表示して、プロパティのほとんどはに基づいてまたは元のメッセージのプロパティから直接コピーします。</span><span class="sxs-lookup"><span data-stu-id="13c0e-109">The main difference between creating a message to be forwarded and creating the original is that with a forwarded message, most of the properties are either based on or copied directly from properties of the original message.</span></span> 
  
<span data-ttu-id="13c0e-110">**メッセージを転送するには**</span><span class="sxs-lookup"><span data-stu-id="13c0e-110">**To forward a message**</span></span>
  
1. <span data-ttu-id="13c0e-111">既定のメッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="13c0e-111">Open the default message store.</span></span> <span data-ttu-id="13c0e-112">詳細については、[既定のメッセージ ストアを開く](opening-the-default-message-store.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13c0e-112">For more information, see [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="13c0e-113">[送信トレイ] フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="13c0e-113">Open the Outbox folder.</span></span> <span data-ttu-id="13c0e-114">詳細については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13c0e-114">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="13c0e-115">新しい転送されたメッセージを作成するのには、[送信トレイ] の[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-115">Call the Outbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new forwarded message.</span></span> 
    
4. <span data-ttu-id="13c0e-116">転送メッセージに次のプロパティをコピーするのには、元のメッセージの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-116">Call the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the following properties to the forwarded message:</span></span> 
    
   - <span data-ttu-id="13c0e-117">**PR\_本文**([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) は、リッチ テキスト形式、テキスト形式または HTML をサポートするかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="13c0e-117">**PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), depending on whether or not you support Rich Text Format, plain text, or HTML.</span></span>
    
   - <span data-ttu-id="13c0e-118">**PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-118">**PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span> 
    
5. <span data-ttu-id="13c0e-119">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティをコピーするのには、元のメッセージの**IMAPIProp::CopyTo**メソッドを呼び出すか、次を呼び出すことによって、元のメッセージからメッセージの添付ファイルをコピーします。各添付ファイルをコピーするための手順を次の 3 つのステップ:</span><span class="sxs-lookup"><span data-stu-id="13c0e-119">Copy the message attachments from the original message either by calling the original message's **IMAPIProp::CopyTo** method to copy the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property or by invoking the following three step procedure for each attachment to be copied:</span></span>
    
   1. <span data-ttu-id="13c0e-120">新しい転送の新しい添付ファイルを作成するのには、メッセージの[IMessage::CreateAttach](imessage-createattach.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-120">Call the new forwarded message's [IMessage::CreateAttach](imessage-createattach.md) method to create a new attachment.</span></span> 
      
   2. <span data-ttu-id="13c0e-121">コピーする添付ファイルを開くには元のメッセージの[IMessage::OpenAttach](imessage-openattach.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-121">Call the original message's [IMessage::OpenAttach](imessage-openattach.md) method to open the attachment to be copied.</span></span> 
      
   3. <span data-ttu-id="13c0e-122">新しいものに古い添付ファイルからすべての添付ファイルのプロパティをコピーするのには、元のメッセージの**IMAPIProp::CopyTo**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-122">Call the original message's **IMAPIProp::CopyTo** method to copy all of the attachment properties from the old attachment to the new one.</span></span> 
    
6. <span data-ttu-id="13c0e-123">**IMAPIProp::CopyTo**を呼び出すには次のプロパティは含まれません。</span><span class="sxs-lookup"><span data-stu-id="13c0e-123">Do not include the following properties in your call to **IMAPIProp::CopyTo**:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="13c0e-124">**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-124">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="13c0e-125">**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-125">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="13c0e-126">**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-126">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="13c0e-127">**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-127">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="13c0e-128">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-128">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="13c0e-129">**PR_RCVD_REPRESENTING**プロパティ</span><span class="sxs-lookup"><span data-stu-id="13c0e-129">**PR_RCVD_REPRESENTING** properties</span></span>  <br/> |
|<span data-ttu-id="13c0e-130">**PR_READ_RECEIPT_ENTRYID**([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-130">**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="13c0e-131">**PR_READ_RECEIPT_REQUESTED**([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-131">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="13c0e-132">**PR_RECEIVED_BY**プロパティ</span><span class="sxs-lookup"><span data-stu-id="13c0e-132">**PR_RECEIVED_BY** properties</span></span>  <br/> |<span data-ttu-id="13c0e-133">**PR_REPLY_RECIPIENT**プロパティ</span><span class="sxs-lookup"><span data-stu-id="13c0e-133">**PR_REPLY_RECIPIENT** properties</span></span>  <br/> |
|<span data-ttu-id="13c0e-134">**PR_REPORT_ENTRYID**([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-134">**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="13c0e-135">**PR_SENDER**プロパティ</span><span class="sxs-lookup"><span data-stu-id="13c0e-135">**PR_SENDER** properties</span></span>  <br/> |
|<span data-ttu-id="13c0e-136">**PR_SENT_REPRESENTING**プロパティ</span><span class="sxs-lookup"><span data-stu-id="13c0e-136">**PR_SENT_REPRESENTING** properties</span></span>  <br/> |<span data-ttu-id="13c0e-137">**PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-137">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="13c0e-138">**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13c0e-138">**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))</span></span>  <br/> | <br/> |
   
1. <span data-ttu-id="13c0e-139">インデントされ、元の送信者を含むヘッダーの段落を追加することによってメッセージのテキストを書式設定の転送、件名、および受信者の一覧の日付。</span><span class="sxs-lookup"><span data-stu-id="13c0e-139">Format the message text by adding indentation and a header paragraph that includes the original sender, date of transmission, subject, and recipient list.</span></span> <span data-ttu-id="13c0e-140">コンテンツとインターネット スタイルの先頭の文字を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="13c0e-140">Do not include Internet-style prefix characters with the content.</span></span>
    
2. <span data-ttu-id="13c0e-141">[ScCreateConversationIndex](sccreateconversationindex.md)、元のメッセージの**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) のプロパティの値を渡してを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-141">Call [ScCreateConversationIndex](sccreateconversationindex.md), passing in the value of the original message's **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="13c0e-142">転送メッセージのプレフィックスを設定します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-142">Set a prefix for the forwarded message.</span></span> <span data-ttu-id="13c0e-143">標準を使用している場合"FW:"、 **PR_NORMALIZED_SUBJECT**の先頭にこれらの文字を連結し、この新しい文字列に**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) を設定します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-143">If you are using the standard "FW:", concatenate these characters onto the beginning of **PR_NORMALIZED_SUBJECT** and set **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) to this new string.</span></span> <span data-ttu-id="13c0e-144">**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) を設定することはしません。</span><span class="sxs-lookup"><span data-stu-id="13c0e-144">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)).</span></span> <span data-ttu-id="13c0e-145">3 文字より長い文字列などの非標準のプレフィックスを使用している場合は、**されて**に格納します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-145">If you are using a nonstandard prefix, such as a string longer than three characters, store it in **PR_SUBJECT_PREFIX**.</span></span> 
    
4. <span data-ttu-id="13c0e-146">**PR_RCVD_REPRESENTING**プロパティに対応する値には、 **PR_SENT_REPRESENTING**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-146">Set the **PR_SENT_REPRESENTING** properties to the corresponding values in the **PR_RCVD_REPRESENTING** properties.</span></span> 
    
5. <span data-ttu-id="13c0e-147">受信者リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-147">Create a recipient list.</span></span> <span data-ttu-id="13c0e-148">詳細については、[受信者リストを作成する](creating-a-recipient-list.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13c0e-148">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
6. <span data-ttu-id="13c0e-149">または保存し、送信する[IMessage::SubmitMessage](imessage-submitmessage.md)を保存するのには、転送されたメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13c0e-149">Call the forwarded message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it or [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send it.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="13c0e-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="13c0e-150">See also</span></span>

- [<span data-ttu-id="13c0e-151">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="13c0e-151">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)

