---
title: メッセージを削除する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316836"
---
# <a name="deleting-a-message"></a><span data-ttu-id="b3179-103">メッセージを削除する</span><span class="sxs-lookup"><span data-stu-id="b3179-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="b3179-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3179-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3179-105">クライアントは開いているメッセージを削除することができ、ユーザーがメッセージを読んでいるとき、または閉じているときに、ユーザーが [コンテンツ] テーブルを表示しているときに、そのメッセージを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="b3179-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="b3179-106">ユーザーが誤ってメッセージを削除しないようにするために、MAPI はメッセージの削除を2段階の手順で定義します。</span><span class="sxs-lookup"><span data-stu-id="b3179-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="b3179-107">削除済みアイテムフォルダーとして指定されているフォルダー ( **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) プロパティにエントリ識別子が格納されているフォルダー) にメッセージを移動するようにマークします。</span><span class="sxs-lookup"><span data-stu-id="b3179-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="b3179-108">[imapifolder::D eletemessages](imapifolder-deletemessages.md)メソッドを呼び出して、メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="b3179-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="b3179-109">削除済みアイテムフォルダー以外のフォルダーにあるメッセージを削除することをユーザーが選択した場合は、削除対象としてマークします。</span><span class="sxs-lookup"><span data-stu-id="b3179-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="b3179-110">ユーザーが [削除済みアイテム] フォルダー内からメッセージを選択した場合にのみ、メッセージがワークステーションから物理的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="b3179-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="b3179-111">ユーザーに本当に削除を実行しているかどうかを確認するように求めるメッセージを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b3179-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="b3179-112">**メッセージを削除するには**</span><span class="sxs-lookup"><span data-stu-id="b3179-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="b3179-113">その後の削除が意図的なものであることをユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="b3179-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="b3179-114">削除するフォルダーの親を決定します。</span><span class="sxs-lookup"><span data-stu-id="b3179-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="b3179-115">削除済みアイテムフォルダーまたは削除済みアイテムフォルダー内のサブフォルダーである場合は、 [imapifolder::D eletemessages](imapifolder-deletemessages.md)を呼び出してメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="b3179-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="b3179-116">フォルダーが [削除済みアイテム] フォルダーに含まれていない場合は、MESSAGE_MOVE フラグが設定された[imapifolder:: copymessages](imapifolder-copymessages.md)を呼び出して、メッセージを削除済みアイテムフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="b3179-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

