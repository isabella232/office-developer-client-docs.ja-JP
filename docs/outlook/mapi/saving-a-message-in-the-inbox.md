---
title: 受信トレイへのメッセージの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3c48ded73d924a400632a94feab65f7afca6e526
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803791"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="84df7-103">受信トレイへのメッセージの保存</span><span class="sxs-lookup"><span data-stu-id="84df7-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="84df7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84df7-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="84df7-105">**いずれかの受信者に受信トレイにメッセージを格納するには**</span><span class="sxs-lookup"><span data-stu-id="84df7-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="84df7-106">受信トレイのエントリ id を取得するために[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="84df7-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="84df7-107">受信トレイを開き、それへのポインターを取得する[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="84df7-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="84df7-108">メッセージを作成するのには、受信トレイの[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="84df7-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="84df7-109">**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、 **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) と**あるの PR_SUBJECT** ([を追加するのには、メッセージの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すPidTagSubject](pidtagsubject-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="84df7-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="84df7-110">各添付ファイルを作成、そのプロパティを設定し、それを保存します。</span><span class="sxs-lookup"><span data-stu-id="84df7-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="84df7-111">メッセージに添付ファイルを追加する方法の詳細については、[メッセージの添付ファイルを作成する](creating-a-message-attachment.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84df7-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="84df7-112">メッセージを保存するのには**IMessage::SaveChanges**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="84df7-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="84df7-113">この時点で、受信トレイの内容のテーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="84df7-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="84df7-114">メッセージ intermittantly を保存する前に、受信トレイの内容のテーブルに表示する場合は、IPM サブツリーのルート フォルダーなどの非表示のフォルダーの代わりに作成し、受信トレイに移動します。</span><span class="sxs-lookup"><span data-stu-id="84df7-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

