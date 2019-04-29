---
title: メッセージの転送
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d1df84c37cc2a24806c35ae0c90e4bf2a5e438d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433179"
---
# <a name="forwarding-a-message"></a><span data-ttu-id="16d7c-103">メッセージの転送</span><span class="sxs-lookup"><span data-stu-id="16d7c-103">Forwarding a message</span></span>

<span data-ttu-id="16d7c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16d7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16d7c-105">メッセージを転送すると、元のメッセージを送信するのと同じタスクが多く行われます。</span><span class="sxs-lookup"><span data-stu-id="16d7c-105">Forwarding a message involves many of the same tasks as sending an original message.</span></span> <span data-ttu-id="16d7c-106">最初に、既定のメッセージストアと、送信メッセージ (通常は送信トレイ) を保持するように指定されているフォルダーを開き、転送するメッセージを作成するために、このフォルダーの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-106">First, you must open the default message store and the folder that is designated to hold outgoing messages, typically the Outbox, and call this folder's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message to be forwarded.</span></span> <span data-ttu-id="16d7c-107">また、元のメッセージを保持するフォルダー (通常は受信トレイ) も開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="16d7c-107">You must also open the folder that holds the original message, typically the Inbox.</span></span> <span data-ttu-id="16d7c-108">別のフォルダーを開く方法については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16d7c-108">For information about opening different folders, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
  
<span data-ttu-id="16d7c-109">転送されるメッセージを作成し、元のメッセージを作成することの主な違いは、転送されたメッセージでは、ほとんどのプロパティが元のメッセージのプロパティから直接またはコピーされるかのどちらかです。</span><span class="sxs-lookup"><span data-stu-id="16d7c-109">The main difference between creating a message to be forwarded and creating the original is that with a forwarded message, most of the properties are either based on or copied directly from properties of the original message.</span></span> 
  
<span data-ttu-id="16d7c-110">**メッセージを転送するには**</span><span class="sxs-lookup"><span data-stu-id="16d7c-110">**To forward a message**</span></span>
  
1. <span data-ttu-id="16d7c-111">既定のメッセージストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="16d7c-111">Open the default message store.</span></span> <span data-ttu-id="16d7c-112">詳細については、「[既定のメッセージストアを開く](opening-the-default-message-store.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16d7c-112">For more information, see [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="16d7c-113">[送信トレイ] フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="16d7c-113">Open the Outbox folder.</span></span> <span data-ttu-id="16d7c-114">詳細については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16d7c-114">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="16d7c-115">送信トレイの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出して、新しい転送メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-115">Call the Outbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new forwarded message.</span></span> 
    
4. <span data-ttu-id="16d7c-116">元のメッセージの[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを呼び出して、次のプロパティを転送されたメッセージにコピーします。</span><span class="sxs-lookup"><span data-stu-id="16d7c-116">Call the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the following properties to the forwarded message:</span></span> 
    
   - <span data-ttu-id="16d7c-117">**\_** リッチテキスト形式、プレーンテキスト、または HTML をサポートしているかどうかに応じて、pr 本文 ([PidTagBody](pidtagbody-canonical-property.md))、 **pr\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) を使用します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-117">**PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), depending on whether or not you support Rich Text Format, plain text, or HTML.</span></span>
    
   - <span data-ttu-id="16d7c-118">**PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-118">**PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span> 
    
5. <span data-ttu-id="16d7c-119">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティをコピーするか、または次のように呼び出して、元の message の**imapiprop:: CopyTo**メソッドを呼び出して、メッセージの添付ファイルを元のメッセージからコピーします。コピーする添付ファイルごとに、次の3つの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-119">Copy the message attachments from the original message either by calling the original message's **IMAPIProp::CopyTo** method to copy the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property or by invoking the following three step procedure for each attachment to be copied:</span></span>
    
   1. <span data-ttu-id="16d7c-120">新しい転送メッセージの[IMessage:: createattach](imessage-createattach.md)メソッドを呼び出して、新しい添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-120">Call the new forwarded message's [IMessage::CreateAttach](imessage-createattach.md) method to create a new attachment.</span></span> 
      
   2. <span data-ttu-id="16d7c-121">元のメッセージの[IMessage:: openattach](imessage-openattach.md)メソッドを呼び出して、コピーする添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="16d7c-121">Call the original message's [IMessage::OpenAttach](imessage-openattach.md) method to open the attachment to be copied.</span></span> 
      
   3. <span data-ttu-id="16d7c-122">元のメッセージの**imapiprop:: CopyTo**メソッドを呼び出して、すべての添付ファイルプロパティを古い添付ファイルから新しい添付ファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="16d7c-122">Call the original message's **IMAPIProp::CopyTo** method to copy all of the attachment properties from the old attachment to the new one.</span></span> 
    
6. <span data-ttu-id="16d7c-123">**imapiprop:: CopyTo**に対する呼び出しには、次のプロパティを含めないでください。</span><span class="sxs-lookup"><span data-stu-id="16d7c-123">Do not include the following properties in your call to **IMAPIProp::CopyTo**:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="16d7c-124">**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-124">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="16d7c-125">**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-125">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="16d7c-126">**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-126">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="16d7c-127">**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-127">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="16d7c-128">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-128">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="16d7c-129">**PR_RCVD_REPRESENTING**プロパティ</span><span class="sxs-lookup"><span data-stu-id="16d7c-129">**PR_RCVD_REPRESENTING** properties</span></span>  <br/> |
|<span data-ttu-id="16d7c-130">**PR_READ_RECEIPT_ENTRYID**([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-130">**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="16d7c-131">**PR_READ_RECEIPT_REQUESTED**([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-131">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="16d7c-132">**PR_RECEIVED_BY**プロパティ</span><span class="sxs-lookup"><span data-stu-id="16d7c-132">**PR_RECEIVED_BY** properties</span></span>  <br/> |<span data-ttu-id="16d7c-133">**PR_REPLY_RECIPIENT**プロパティ</span><span class="sxs-lookup"><span data-stu-id="16d7c-133">**PR_REPLY_RECIPIENT** properties</span></span>  <br/> |
|<span data-ttu-id="16d7c-134">**PR_REPORT_ENTRYID**([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-134">**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="16d7c-135">**PR_SENDER**プロパティ</span><span class="sxs-lookup"><span data-stu-id="16d7c-135">**PR_SENDER** properties</span></span>  <br/> |
|<span data-ttu-id="16d7c-136">**PR_SENT_REPRESENTING**プロパティ</span><span class="sxs-lookup"><span data-stu-id="16d7c-136">**PR_SENT_REPRESENTING** properties</span></span>  <br/> |<span data-ttu-id="16d7c-137">**PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-137">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="16d7c-138">**PR_SUBJECT_PREFIX**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16d7c-138">**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))</span></span>  <br/> | <br/> |
   
1. <span data-ttu-id="16d7c-139">メッセージテキストの書式を設定するインデントと、元の送信者、送信日、件名、および受信者リストを含むヘッダー段落を追加します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-139">Format the message text by adding indentation and a header paragraph that includes the original sender, date of transmission, subject, and recipient list.</span></span> <span data-ttu-id="16d7c-140">コンテンツにインターネットスタイルのプレフィックス文字を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="16d7c-140">Do not include Internet-style prefix characters with the content.</span></span>
    
2. <span data-ttu-id="16d7c-141">[ScCreateConversationIndex](sccreateconversationindex.md)を呼び出し、元のメッセージの**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-141">Call [ScCreateConversationIndex](sccreateconversationindex.md), passing in the value of the original message's **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="16d7c-142">転送されるメッセージのプレフィックスを設定します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-142">Set a prefix for the forwarded message.</span></span> <span data-ttu-id="16d7c-143">標準の "FW:" を使用している場合は、これらの文字を**PR_NORMALIZED_SUBJECT**の先頭に連結し、 **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) をこの新しい文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-143">If you are using the standard "FW:", concatenate these characters onto the beginning of **PR_NORMALIZED_SUBJECT** and set **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) to this new string.</span></span> <span data-ttu-id="16d7c-144">**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) を設定しません。</span><span class="sxs-lookup"><span data-stu-id="16d7c-144">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)).</span></span> <span data-ttu-id="16d7c-145">3文字を超える文字列など、標準的ではないプリフィックスを使用している場合は、 **PR_SUBJECT_PREFIX**に格納します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-145">If you are using a nonstandard prefix, such as a string longer than three characters, store it in **PR_SUBJECT_PREFIX**.</span></span> 
    
4. <span data-ttu-id="16d7c-146">**PR_SENT_REPRESENTING**プロパティを**PR_RCVD_REPRESENTING**プロパティの対応する値に設定します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-146">Set the **PR_SENT_REPRESENTING** properties to the corresponding values in the **PR_RCVD_REPRESENTING** properties.</span></span> 
    
5. <span data-ttu-id="16d7c-147">受信者リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-147">Create a recipient list.</span></span> <span data-ttu-id="16d7c-148">詳細については、「[受信者リストを作成](creating-a-recipient-list.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16d7c-148">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
6. <span data-ttu-id="16d7c-149">転送されたメッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して保存します。また、 [IMessage:: submitmessage](imessage-submitmessage.md)に保存して送信します。</span><span class="sxs-lookup"><span data-stu-id="16d7c-149">Call the forwarded message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it or [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send it.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="16d7c-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="16d7c-150">See also</span></span>

- [<span data-ttu-id="16d7c-151">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="16d7c-151">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)

