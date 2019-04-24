---
title: 受信トレイへのメッセージの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357534"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="e0b5b-103">受信トレイへのメッセージの保存</span><span class="sxs-lookup"><span data-stu-id="e0b5b-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="e0b5b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0b5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e0b5b-105">**受信者なしでメッセージを受信トレイに保存するには**</span><span class="sxs-lookup"><span data-stu-id="e0b5b-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="e0b5b-106">[IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を呼び出して、受信トレイのエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="e0b5b-107">[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、受信トレイを開き、そのアドレスへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="e0b5b-108">受信トレイの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出して、メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="e0b5b-109">メッセージの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、 **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))、PR_SUBJECT ()、()、 \*\*\*\* () を追加します ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="e0b5b-110">各添付ファイルを作成し、そのプロパティを設定して保存します。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="e0b5b-111">メッセージに添付ファイルを追加する方法の詳細については、「[メッセージの添付ファイルを作成](creating-a-message-attachment.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="e0b5b-112">メッセージを保存するには、 **IMessage:: SaveChanges**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="e0b5b-113">この時点で、受信トレイのコンテンツテーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="e0b5b-114">受信トレイのコンテンツテーブルにメッセージを表示する前に、intermittantly メッセージを保存する場合は、代わりに、IPM サブツリーのルートフォルダーなどの隠しフォルダーで作成し、受信トレイに移動します。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

