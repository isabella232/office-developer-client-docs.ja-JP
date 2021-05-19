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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421222"
---
# <a name="ipm-subtree"></a><span data-ttu-id="8efca-103">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="8efca-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="8efca-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8efca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8efca-105">MAPI は、コンピューターの受信者ではなく、人間にメッセージを送受信するすべてのクライアントのメッセージ ストアのルート フォルダーの下にフォルダーのツリーを作成します。</span><span class="sxs-lookup"><span data-stu-id="8efca-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="8efca-106">人間の受信者間で交換されるメッセージは対人メッセージと呼び、このツリーは対人間メッセージ (IPM) サブツリーと呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="8efca-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="8efca-107">配信ストアの IPM サブツリーは、少なくとも次のフォルダーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="8efca-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="8efca-108">受信トレイ</span><span class="sxs-lookup"><span data-stu-id="8efca-108">Inbox</span></span>
    
- <span data-ttu-id="8efca-109">送信トレイ</span><span class="sxs-lookup"><span data-stu-id="8efca-109">Outbox</span></span>
    
- <span data-ttu-id="8efca-110">送信済みアイテム</span><span class="sxs-lookup"><span data-stu-id="8efca-110">Sent Items</span></span>
    
- <span data-ttu-id="8efca-111">削除済みアイテム</span><span class="sxs-lookup"><span data-stu-id="8efca-111">Deleted Items</span></span>
    
<span data-ttu-id="8efca-112">これらは、これらの各フォルダーの既定の名前と役割です。既定の名前が適切ではない場合、クライアントは独自の名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8efca-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="8efca-113">MAPI は、クライアントがメッセージの受信フォルダーの確立を怠った場合に、メッセージが誤って消えてしまうのを回避するために、これらのフォルダーの既定の名前と関連付けを割り当てします。</span><span class="sxs-lookup"><span data-stu-id="8efca-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="8efca-114">このコンテキストMicrosoft Office Outlook IPM サブツリーは、予定表、連絡先、タスク、メモ、およびジャーナル用の追加の既定のフォルダーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="8efca-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="8efca-115">受信トレイには通常、受信メッセージが保持され、送信トレイには送信メッセージ (つまり、送信待ちメッセージ) が保持されます。</span><span class="sxs-lookup"><span data-stu-id="8efca-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="8efca-116">クライアントが **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティをこのフォルダーのエントリ識別子に設定している場合は、送信された各メッセージのコピーが送信されたアイテム フォルダーに保持されます。</span><span class="sxs-lookup"><span data-stu-id="8efca-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="8efca-117">[削除済みアイテム] フォルダーには、削除のマークが付いたメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8efca-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8efca-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="8efca-118">See also</span></span>



<span data-ttu-id="8efca-119">[MAPI �t�H���_�[](mapi-folders.md)</span><span class="sxs-lookup"><span data-stu-id="8efca-119">[MAPI Folders](mapi-folders.md)</span></span>

