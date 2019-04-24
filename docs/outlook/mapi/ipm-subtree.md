---
title: IPM サブツリー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317109"
---
# <a name="ipm-subtree"></a><span data-ttu-id="bace3-103">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="bace3-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="bace3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bace3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bace3-105">MAPI は、メッセージをコンピューターや受信者ではなく、人間との間で送受信するすべてのクライアントに対して、メッセージストアのルートフォルダーの下にフォルダーのツリーを作成します。</span><span class="sxs-lookup"><span data-stu-id="bace3-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="bace3-106">人間の受信者間で交換されるメッセージは、個人間メッセージと呼ばれ、このツリーは個人間メッセージ (IPM、サブツリー) と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="bace3-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="bace3-107">配信ストアの IPM サブツリーは、少なくとも次のフォルダーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="bace3-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="bace3-108">Inbox</span><span class="sxs-lookup"><span data-stu-id="bace3-108">Inbox</span></span>
    
- <span data-ttu-id="bace3-109">送信トレイ</span><span class="sxs-lookup"><span data-stu-id="bace3-109">Outbox</span></span>
    
- <span data-ttu-id="bace3-110">送信済みアイテム</span><span class="sxs-lookup"><span data-stu-id="bace3-110">Sent Items</span></span>
    
- <span data-ttu-id="bace3-111">削除済みアイテム</span><span class="sxs-lookup"><span data-stu-id="bace3-111">Deleted Items</span></span>
    
<span data-ttu-id="bace3-112">これらの各フォルダーの既定の名前とロールは次のとおりです。クライアントは、既定の名前が適切でない場合、独自の名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="bace3-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="bace3-113">MAPI では、クライアント戻さがメッセージの受信フォルダーを確立するときに、メッセージが誤って消失しないようにするために、これらのフォルダーに既定の名前と関連付けが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="bace3-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="bace3-114">Microsoft Office Outlook のコンテキストでは、IPM サブツリーは、予定表、連絡先、タスク、メモ、およびジャーナルの追加の既定のフォルダーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="bace3-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="bace3-115">通常、受信トレイは受信メッセージを保持し、送信トレイは送信メッセージを保持します (つまり、送信を待機しているメッセージ)。</span><span class="sxs-lookup"><span data-stu-id="bace3-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="bace3-116">クライアントが**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティをこのフォルダーのエントリ識別子に設定している場合、送信済みアイテムフォルダーには、送信された各メッセージのコピーが保持されます。</span><span class="sxs-lookup"><span data-stu-id="bace3-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="bace3-117">削除済みアイテムフォルダーには、削除のマークが付いたメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bace3-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bace3-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="bace3-118">See also</span></span>



<span data-ttu-id="bace3-119">[MAPI �t�H���_�[](mapi-folders.md)</span><span class="sxs-lookup"><span data-stu-id="bace3-119">[MAPI Folders](mapi-folders.md)</span></span>

