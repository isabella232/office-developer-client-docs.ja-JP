---
title: メッセージを投稿
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 33bf6780979ee25739abf93d89744e1517363c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803692"
---
# <a name="posting-a-message"></a><span data-ttu-id="644da-103">メッセージを投稿</span><span class="sxs-lookup"><span data-stu-id="644da-103">Posting a message</span></span>

<span data-ttu-id="644da-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="644da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="644da-105">メッセージを投稿することは、メッセージを送信することに似ています。</span><span class="sxs-lookup"><span data-stu-id="644da-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="644da-106">主な違いは、リンク先です。</span><span class="sxs-lookup"><span data-stu-id="644da-106">The main difference is the destination.</span></span> <span data-ttu-id="644da-107">1 つまたは複数のメッセージング システム間で 1 つまたは複数の受信者に送信されるのではなく、現在のメッセージ ストア内のフォルダーに投稿されたメッセージのままです。</span><span class="sxs-lookup"><span data-stu-id="644da-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="644da-108">メッセージを投稿するには</span><span class="sxs-lookup"><span data-stu-id="644da-108">To post a message</span></span>
  
1. <span data-ttu-id="644da-109">[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出すことによって、コピー先のフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="644da-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="644da-110">コピー先のフォルダーが受信トレイの場合は、 [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出すことによって**OpenEntry**に渡すためのエントリ id を検索します。</span><span class="sxs-lookup"><span data-stu-id="644da-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="644da-111">メッセージを作成するのには[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="644da-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="644da-112">メソッドを呼び出してメッセージの[IMAPIProp::SetProps](imapiprop-setprops.md)を設定します。</span><span class="sxs-lookup"><span data-stu-id="644da-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="644da-113">**PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) のプロパティに MSGFLAG_READ フラグです。</span><span class="sxs-lookup"><span data-stu-id="644da-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="644da-114">**PR_SENDER**プロパティです。</span><span class="sxs-lookup"><span data-stu-id="644da-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="644da-115">**PR_SENT_REPRESENTING**プロパティです。</span><span class="sxs-lookup"><span data-stu-id="644da-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="644da-116">**PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="644da-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="644da-117">**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティです。</span><span class="sxs-lookup"><span data-stu-id="644da-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="644da-118">**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="644da-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="644da-119">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="644da-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="644da-120">メッセージ クラスに必要なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="644da-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="644da-121">メッセージを保存するのには、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="644da-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="644da-122">必要に応じて、添付ファイルを作成、そのプロパティを設定し、保存します。</span><span class="sxs-lookup"><span data-stu-id="644da-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="644da-123">メッセージに添付ファイルを追加する方法の詳細については、[メッセージの添付ファイルを作成する](creating-a-message-attachment.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="644da-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="644da-124">メッセージを保存するのには**IMessage::SaveChanges**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="644da-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="644da-125">この時点でコピー先のフォルダーの内容のテーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="644da-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="644da-126">受信者リストを作成しないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="644da-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="644da-127">代わりに、送信されたメッセージのトランスポート プロバイダーが正常に設定されているいくつかのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="644da-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="644da-128">断続的にする前に表示されているフォルダーの内容のテーブルに表示されるメッセージを保存する場合は、IPM サブツリーのルート フォルダーなどの非表示のフォルダーの代わりに作成し、ターゲット フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="644da-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

