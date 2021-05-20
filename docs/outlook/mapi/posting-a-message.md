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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429769"
---
# <a name="posting-a-message"></a><span data-ttu-id="58b5b-103">メッセージの投稿</span><span class="sxs-lookup"><span data-stu-id="58b5b-103">Posting a message</span></span>

<span data-ttu-id="58b5b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58b5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58b5b-105">メッセージの投稿は、メッセージの送信に似ています。</span><span class="sxs-lookup"><span data-stu-id="58b5b-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="58b5b-106">主な違いは宛先です。</span><span class="sxs-lookup"><span data-stu-id="58b5b-106">The main difference is the destination.</span></span> <span data-ttu-id="58b5b-107">1 つ以上のメッセージング システムで 1 つ以上の受信者に送信されるのではなく、投稿されたメッセージは現在のメッセージ ストア内のフォルダーに残ります。</span><span class="sxs-lookup"><span data-stu-id="58b5b-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="58b5b-108">メッセージを投稿するには</span><span class="sxs-lookup"><span data-stu-id="58b5b-108">To post a message</span></span>
  
1. <span data-ttu-id="58b5b-109">[IMsgStore::OpenEntry を呼び出して、移動先フォルダーを開きます](imsgstore-openentry.md)。</span><span class="sxs-lookup"><span data-stu-id="58b5b-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="58b5b-110">宛先フォルダーが受信トレイの場合は [、IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出して **OpenEntry** に渡すエントリ識別子を探します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="58b5b-111">[IMAPIFolder::CreateMessage を呼び出して](imapifolder-createmessage.md)メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="58b5b-112">メッセージの [IMAPIProp::SetProps メソッドを呼び出して設定](imapiprop-setprops.md) します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="58b5b-113">MSGFLAG_READ **PidTagMessageFlags** [(](pidtagmessageflags-canonical-property.md)PR_MESSAGE_FLAGS ) プロパティPR_MESSAGE_FLAGSフラグです。</span><span class="sxs-lookup"><span data-stu-id="58b5b-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="58b5b-114">プロパティ **PR_SENDER** します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="58b5b-115">プロパティ **PR_SENT_REPRESENTING** します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="58b5b-116">プロパティ **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="58b5b-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="58b5b-117">プロパティ **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または PR_BODY **(** [PidTagBody](pidtagbody-canonical-property.md)) プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="58b5b-118">プロパティ **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="58b5b-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="58b5b-119">プロパティ **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="58b5b-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="58b5b-120">メッセージ クラスで必要なプロパティ。</span><span class="sxs-lookup"><span data-stu-id="58b5b-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="58b5b-121">メッセージを保存するには、 [メッセージの IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="58b5b-122">必要に応じて、添付ファイルを作成し、そのプロパティを設定し、保存します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="58b5b-123">メッセージへの添付ファイルの追加の詳細については、「メッセージ添付ファイルの [作成」を参照してください](creating-a-message-attachment.md)。</span><span class="sxs-lookup"><span data-stu-id="58b5b-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="58b5b-124">**IMessage::SaveChanges を呼び出して** メッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="58b5b-125">この時点で、移動先フォルダーのコンテンツ テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="58b5b-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="58b5b-126">受信者リストを作成しない場合に注意してください。</span><span class="sxs-lookup"><span data-stu-id="58b5b-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="58b5b-127">代わりに、送信メッセージに対してトランスポート プロバイダーによって通常設定されるいくつかのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="58b5b-128">メッセージを表示フォルダーのコンテンツ テーブルに表示する前に断続的に保存する場合は、IPM サブツリーのルート フォルダーなどの非表示フォルダーにメッセージを作成し、ターゲット フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="58b5b-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

