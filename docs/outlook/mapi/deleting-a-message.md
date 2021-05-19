---
title: メッセージの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433165"
---
# <a name="deleting-a-message"></a><span data-ttu-id="98327-103">メッセージの削除</span><span class="sxs-lookup"><span data-stu-id="98327-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="98327-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98327-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98327-105">クライアントは、メッセージが開いているときに、ユーザーがメッセージを読み取る場合、またはメッセージが閉じ、ユーザーがコンテンツ テーブルを表示している場合に削除できます。</span><span class="sxs-lookup"><span data-stu-id="98327-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="98327-106">ユーザーが誤ってメッセージを削除することを保護するために、MAPI はメッセージの削除を 2 つの手順プロセスとして定義します。</span><span class="sxs-lookup"><span data-stu-id="98327-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="98327-107">削除済みアイテム フォルダーとして指定されているフォルダー (エントリ識別子が **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)プロパティに格納されているフォルダー) に移動して、削除メッセージをマークします。</span><span class="sxs-lookup"><span data-stu-id="98327-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="98327-108">[IMAPIFolder::D eleteMessages メソッドを呼び出して、メッセージを削除](imapifolder-deletemessages.md)します。</span><span class="sxs-lookup"><span data-stu-id="98327-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="98327-109">ユーザーが [削除済みアイテム] フォルダー以外のフォルダー内のメッセージを削除する場合は、削除のマークを付きます。</span><span class="sxs-lookup"><span data-stu-id="98327-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="98327-110">ユーザーが削除済みアイテム フォルダー内からメッセージを選択した場合にのみ、メッセージをワークステーションから物理的に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98327-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="98327-111">ユーザーに対して、削除を実際に実行する意図を確認するように求めるメッセージを表示できます。</span><span class="sxs-lookup"><span data-stu-id="98327-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="98327-112">**メッセージを削除するには**</span><span class="sxs-lookup"><span data-stu-id="98327-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="98327-113">差し迫った削除が意図的な場合は、ユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="98327-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="98327-114">削除するフォルダーの親を決定します。</span><span class="sxs-lookup"><span data-stu-id="98327-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="98327-115">削除済みアイテム フォルダーまたは削除済みアイテム フォルダー内のサブフォルダーである場合は [、IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) を呼び出してメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="98327-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="98327-116">フォルダーが削除済みアイテム フォルダー内に含まれている場合は、メッセージを削除済みアイテム フォルダーに再配置するために、MESSAGE_MOVE フラグが設定された [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98327-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

