---
title: メッセージの投稿
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350751"
---
# <a name="posting-a-message"></a><span data-ttu-id="6d1fe-103">メッセージの投稿</span><span class="sxs-lookup"><span data-stu-id="6d1fe-103">Posting a message</span></span>

<span data-ttu-id="6d1fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d1fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d1fe-105">メッセージを投稿することは、メッセージの送信と似ています。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="6d1fe-106">主な違いは、宛先です。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-106">The main difference is the destination.</span></span> <span data-ttu-id="6d1fe-107">1つまたは複数のメッセージングシステムで1人または複数の受信者に転送されるのではなく、現在のメッセージストア内のフォルダーに投稿されたメッセージが残っています。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="6d1fe-108">メッセージを投稿するには</span><span class="sxs-lookup"><span data-stu-id="6d1fe-108">To post a message</span></span>
  
1. <span data-ttu-id="6d1fe-109">[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、宛先フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="6d1fe-110">宛先フォルダーが受信トレイの場合は、 [IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を呼び出して**openentry**に渡すエントリ識別子を見つけます。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="6d1fe-111">[imapifolder:: CreateMessage](imapifolder-createmessage.md)を呼び出して、メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="6d1fe-112">メッセージの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="6d1fe-113">**PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグ。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="6d1fe-114">**PR_SENDER**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="6d1fe-115">**PR_SENT_REPRESENTING**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="6d1fe-116">**PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="6d1fe-117">**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="6d1fe-118">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="6d1fe-119">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="6d1fe-120">メッセージクラスに必要なすべてのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="6d1fe-121">メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して、メッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="6d1fe-122">必要に応じて、添付ファイルを作成し、そのプロパティを設定して保存します。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="6d1fe-123">メッセージへの添付ファイルの追加の詳細については、「[メッセージの添付ファイルを作成](creating-a-message-attachment.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="6d1fe-124">メッセージを保存するには、 **IMessage:: SaveChanges**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="6d1fe-125">この時点で、移動先フォルダーの contents テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="6d1fe-126">受信者リストは作成されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="6d1fe-127">代わりに、送信されたメッセージのトランスポートプロバイダーによって設定されるプロパティをいくつか設定します。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="6d1fe-128">表示されているフォルダーの contents テーブルにメッセージを表示する前に、メッセージを保存する場合は、そのメッセージを IPM サブツリーのルートフォルダーなどの非表示のフォルダー内に作成して、移動先のフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="6d1fe-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

