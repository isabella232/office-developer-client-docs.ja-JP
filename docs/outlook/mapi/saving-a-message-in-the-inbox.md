---
title: 受信トレイにメッセージを保存する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407894"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="be6bf-103">受信トレイにメッセージを保存する</span><span class="sxs-lookup"><span data-stu-id="be6bf-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="be6bf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be6bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="be6bf-105">**受信者を含めずにメッセージを受信トレイに保存するには**</span><span class="sxs-lookup"><span data-stu-id="be6bf-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="be6bf-106">受信 [トレイのエントリ識別子を取得するには、IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="be6bf-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="be6bf-107">[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出して受信トレイを開き、その受信トレイへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="be6bf-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="be6bf-108">受信トレイの [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="be6bf-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="be6bf-109">メッセージの [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出 **して、PR_BODY** [(PidTagBody)、PR_HTML](pidtagbody-canonical-property.md)[(PidTagHtml)、](pidtaghtml-canonical-property.md)または **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティと **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティを追加します。 </span><span class="sxs-lookup"><span data-stu-id="be6bf-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="be6bf-110">各添付ファイルを作成し、そのプロパティを設定し、保存します。</span><span class="sxs-lookup"><span data-stu-id="be6bf-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="be6bf-111">メッセージへの添付ファイルの追加の詳細については、「メッセージ添付ファイルの作成 [」を参照してください](creating-a-message-attachment.md)。</span><span class="sxs-lookup"><span data-stu-id="be6bf-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="be6bf-112">**IMessage::SaveChanges を呼び出して** メッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="be6bf-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="be6bf-113">この時点で、受信トレイのコンテンツ テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="be6bf-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="be6bf-114">メッセージを受信トレイのコンテンツ テーブルに表示する前に、メッセージを間で保存する場合は、IPM サブツリーのルート フォルダーなどの非表示フォルダーにメッセージを作成し、受信トレイに移動します。</span><span class="sxs-lookup"><span data-stu-id="be6bf-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

