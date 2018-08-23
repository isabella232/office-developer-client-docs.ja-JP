---
title: IPM サブツリー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6fe642d10a50d25874aee170441a07c184b46575
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591094"
---
# <a name="ipm-subtree"></a><span data-ttu-id="6ad23-103">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="6ad23-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="6ad23-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ad23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ad23-105">MAPI は、メッセージの送信し、コンピューターでの受信者ではなく、人間からのメッセージを受信するすべてのクライアントのメッセージ ストアのルート フォルダーの下にフォルダーのツリーを作成します。</span><span class="sxs-lookup"><span data-stu-id="6ad23-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="6ad23-106">人の受信者間で交換されるメッセージは、個人間のメッセージと呼ばれていて、このツリーは、既知の個人間のメッセージでは、IPM とサブツリーです。</span><span class="sxs-lookup"><span data-stu-id="6ad23-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="6ad23-107">IPM サブツリーの配信ストアで構成されています、少なくとも次のフォルダー。</span><span class="sxs-lookup"><span data-stu-id="6ad23-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="6ad23-108">受信トレイ</span><span class="sxs-lookup"><span data-stu-id="6ad23-108">Inbox</span></span>
    
- <span data-ttu-id="6ad23-109">送信トレイ</span><span class="sxs-lookup"><span data-stu-id="6ad23-109">Outbox</span></span>
    
- <span data-ttu-id="6ad23-110">送信済みアイテム</span><span class="sxs-lookup"><span data-stu-id="6ad23-110">Sent Items</span></span>
    
- <span data-ttu-id="6ad23-111">削除済みアイテム</span><span class="sxs-lookup"><span data-stu-id="6ad23-111">Deleted Items</span></span>
    
<span data-ttu-id="6ad23-112">これらは、既定の名前とこれらのフォルダーのそれぞれの役割クライアントは、既定の名前が適切でない場合に独自の名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6ad23-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="6ad23-113">MAPI には、既定の名前とこれらのクライアントがメッセージの受信側のフォルダーを設定しなかった場合に誤って消失からのメッセージを保持するフォルダーの関連付けが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6ad23-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="6ad23-114">コンテキストでは、Microsoft Office Outlook、IPM サブツリーは、追加の既定フォルダーの予定表、連絡先、タスク、メモ、および仕訳帳の。</span><span class="sxs-lookup"><span data-stu-id="6ad23-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="6ad23-115">受信トレイは通常、受信メッセージを保持し、送信トレイに送信メッセージ (つまり、送信待ちメッセージ) が保持しています。</span><span class="sxs-lookup"><span data-stu-id="6ad23-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="6ad23-116">送信済みアイテム フォルダーは、クライアントがこのフォルダーのエントリ id を**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティを設定した場合に、送信済みのメッセージのコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="6ad23-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="6ad23-117">削除済みアイテム フォルダーには、削除用にマークされたメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ad23-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ad23-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ad23-118">See also</span></span>



<span data-ttu-id="6ad23-119">[MAPI �t�H���_�[](mapi-folders.md)</span><span class="sxs-lookup"><span data-stu-id="6ad23-119">[MAPI Folders](mapi-folders.md)</span></span>

