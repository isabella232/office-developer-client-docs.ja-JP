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
# <a name="forwarding-a-message"></a><span data-ttu-id="aa95b-103">メッセージの転送</span><span class="sxs-lookup"><span data-stu-id="aa95b-103">Forwarding a message</span></span>

<span data-ttu-id="aa95b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa95b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa95b-105">メッセージの転送には、元のメッセージの送信と同じタスクの多くが含まれます。</span><span class="sxs-lookup"><span data-stu-id="aa95b-105">Forwarding a message involves many of the same tasks as sending an original message.</span></span> <span data-ttu-id="aa95b-106">最初に、既定のメッセージ ストアと、送信メッセージを保持するために指定されているフォルダー (通常は送信ボックス) を開き、このフォルダーの [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、転送するメッセージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa95b-106">First, you must open the default message store and the folder that is designated to hold outgoing messages, typically the Outbox, and call this folder's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message to be forwarded.</span></span> <span data-ttu-id="aa95b-107">また、元のメッセージを保持するフォルダー (通常は受信トレイ) を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa95b-107">You must also open the folder that holds the original message, typically the Inbox.</span></span> <span data-ttu-id="aa95b-108">異なるフォルダーを開く方法については、「 [メッセージ ストア フォルダーを開く」を参照してください](opening-a-message-store-folder.md)。</span><span class="sxs-lookup"><span data-stu-id="aa95b-108">For information about opening different folders, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
  
<span data-ttu-id="aa95b-109">転送するメッセージを作成し、元のメッセージを作成する主な違いは、転送されたメッセージでは、ほとんどのプロパティが元のメッセージのプロパティに基づくか、元のメッセージのプロパティから直接コピーされるという点です。</span><span class="sxs-lookup"><span data-stu-id="aa95b-109">The main difference between creating a message to be forwarded and creating the original is that with a forwarded message, most of the properties are either based on or copied directly from properties of the original message.</span></span> 
  
<span data-ttu-id="aa95b-110">**メッセージを転送するには**</span><span class="sxs-lookup"><span data-stu-id="aa95b-110">**To forward a message**</span></span>
  
1. <span data-ttu-id="aa95b-111">既定のメッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="aa95b-111">Open the default message store.</span></span> <span data-ttu-id="aa95b-112">詳細については、「既定のメッセージ [ストアを開く」を参照してください](opening-the-default-message-store.md)。</span><span class="sxs-lookup"><span data-stu-id="aa95b-112">For more information, see [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="aa95b-113">[送信ボックス] フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="aa95b-113">Open the Outbox folder.</span></span> <span data-ttu-id="aa95b-114">詳細については、「メッセージ ストア フォルダー [を開く」を参照してください](opening-a-message-store-folder.md)。</span><span class="sxs-lookup"><span data-stu-id="aa95b-114">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="aa95b-115">Outbox の [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、新しい転送メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="aa95b-115">Call the Outbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new forwarded message.</span></span> 
    
4. <span data-ttu-id="aa95b-116">元のメッセージの [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを呼び出して、転送されたメッセージに次のプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="aa95b-116">Call the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the following properties to the forwarded message:</span></span> 
    
   - <span data-ttu-id="aa95b-117">**PR \_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) **、PR \_ HTML** [(PidTagHtml)、](pidtaghtml-canonical-property.md)または PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) は、リッチ テキスト形式、プレーン テキスト、または HTML をサポートするかどうかに応じて異なる。 </span><span class="sxs-lookup"><span data-stu-id="aa95b-117">**PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), depending on whether or not you support Rich Text Format, plain text, or HTML.</span></span>
    
   - <span data-ttu-id="aa95b-118">**PR \_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-118">**PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span> 
    
5. <span data-ttu-id="aa95b-119">元のメッセージの **IMAPIProp::CopyTo** メソッドを呼び出して PR_MESSAGE_ATTACHMENTS ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティをコピーするか、コピーする添付ファイルごとに次の **3** つの手順を実行して、元のメッセージからメッセージ添付ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="aa95b-119">Copy the message attachments from the original message either by calling the original message's **IMAPIProp::CopyTo** method to copy the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property or by invoking the following three step procedure for each attachment to be copied:</span></span>
    
   1. <span data-ttu-id="aa95b-120">新しい転送されたメッセージの [IMessage::CreateAttach](imessage-createattach.md) メソッドを呼び出して、新しい添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="aa95b-120">Call the new forwarded message's [IMessage::CreateAttach](imessage-createattach.md) method to create a new attachment.</span></span> 
      
   2. <span data-ttu-id="aa95b-121">元のメッセージの [IMessage::OpenAttach](imessage-openattach.md) メソッドを呼び出して、コピーする添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="aa95b-121">Call the original message's [IMessage::OpenAttach](imessage-openattach.md) method to open the attachment to be copied.</span></span> 
      
   3. <span data-ttu-id="aa95b-122">元のメッセージの **IMAPIProp::CopyTo** メソッドを呼び出して、すべての添付ファイル プロパティを古い添付ファイルから新しい添付ファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="aa95b-122">Call the original message's **IMAPIProp::CopyTo** method to copy all of the attachment properties from the old attachment to the new one.</span></span> 
    
6. <span data-ttu-id="aa95b-123">**IMAPIProp::CopyTo** への呼び出しには、次のプロパティを含めない。</span><span class="sxs-lookup"><span data-stu-id="aa95b-123">Do not include the following properties in your call to **IMAPIProp::CopyTo**:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="aa95b-124">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-124">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa95b-125">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-125">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="aa95b-126">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-126">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa95b-127">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-127">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="aa95b-128">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-128">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa95b-129">**PR_RCVD_REPRESENTING** プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa95b-129">**PR_RCVD_REPRESENTING** properties</span></span>  <br/> |
|<span data-ttu-id="aa95b-130">**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-130">**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa95b-131">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-131">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="aa95b-132">**PR_RECEIVED_BY** プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa95b-132">**PR_RECEIVED_BY** properties</span></span>  <br/> |<span data-ttu-id="aa95b-133">**PR_REPLY_RECIPIENT** プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa95b-133">**PR_REPLY_RECIPIENT** properties</span></span>  <br/> |
|<span data-ttu-id="aa95b-134">**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-134">**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa95b-135">**PR_SENDER** プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa95b-135">**PR_SENDER** properties</span></span>  <br/> |
|<span data-ttu-id="aa95b-136">**PR_SENT_REPRESENTING** プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa95b-136">**PR_SENT_REPRESENTING** properties</span></span>  <br/> |<span data-ttu-id="aa95b-137">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-137">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="aa95b-138">**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa95b-138">**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))</span></span>  <br/> | <br/> |
   
1. <span data-ttu-id="aa95b-139">インデントと、元の送信者、送信日、件名、受信者リストを含むヘッダー段落を追加して、メッセージ テキストの書式を設定します。</span><span class="sxs-lookup"><span data-stu-id="aa95b-139">Format the message text by adding indentation and a header paragraph that includes the original sender, date of transmission, subject, and recipient list.</span></span> <span data-ttu-id="aa95b-140">コンテンツにインターネット スタイルのプレフィックス文字を含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="aa95b-140">Do not include Internet-style prefix characters with the content.</span></span>
    
2. <span data-ttu-id="aa95b-141">[ScCreateConversationIndex](sccreateconversationindex.md)を呼び出し、元のメッセージのプロパティ[(PidTagConversationIndex)](pidtagconversationindex-canonical-property.md)プロパティPR_CONVERSATION_INDEX値を渡します。</span><span class="sxs-lookup"><span data-stu-id="aa95b-141">Call [ScCreateConversationIndex](sccreateconversationindex.md), passing in the value of the original message's **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="aa95b-142">転送されたメッセージのプレフィックスを設定します。</span><span class="sxs-lookup"><span data-stu-id="aa95b-142">Set a prefix for the forwarded message.</span></span> <span data-ttu-id="aa95b-143">標準の "FW:" を使用している場合は、これらの文字を **PR_NORMALIZED_SUBJECT** の先頭に連結し **、PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) をこの新しい文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="aa95b-143">If you are using the standard "FW:", concatenate these characters onto the beginning of **PR_NORMALIZED_SUBJECT** and set **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) to this new string.</span></span> <span data-ttu-id="aa95b-144">[(PidTagSubjectPrefix)](pidtagsubjectprefix-canonical-property.md) **PR_SUBJECT_PREFIX設定** しない。</span><span class="sxs-lookup"><span data-stu-id="aa95b-144">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)).</span></span> <span data-ttu-id="aa95b-145">3 文字を超える文字列など、標準以外のプレフィックスを使用している場合は、そのプレフィックスを **PR_SUBJECT_PREFIX。**</span><span class="sxs-lookup"><span data-stu-id="aa95b-145">If you are using a nonstandard prefix, such as a string longer than three characters, store it in **PR_SUBJECT_PREFIX**.</span></span> 
    
4. <span data-ttu-id="aa95b-146">プロパティの **PR_SENT_REPRESENTING** プロパティに対応する **値を設定** PR_RCVD_REPRESENTINGします。</span><span class="sxs-lookup"><span data-stu-id="aa95b-146">Set the **PR_SENT_REPRESENTING** properties to the corresponding values in the **PR_RCVD_REPRESENTING** properties.</span></span> 
    
5. <span data-ttu-id="aa95b-147">受信者リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="aa95b-147">Create a recipient list.</span></span> <span data-ttu-id="aa95b-148">詳細については、「受信者リストの [作成」を参照してください](creating-a-recipient-list.md)。</span><span class="sxs-lookup"><span data-stu-id="aa95b-148">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
6. <span data-ttu-id="aa95b-149">転送されたメッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出して保存するか [、IMessage::SubmitMessage](imessage-submitmessage.md) を呼び出して保存して送信します。</span><span class="sxs-lookup"><span data-stu-id="aa95b-149">Call the forwarded message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it or [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send it.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="aa95b-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa95b-150">See also</span></span>

- [<span data-ttu-id="aa95b-151">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa95b-151">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)

