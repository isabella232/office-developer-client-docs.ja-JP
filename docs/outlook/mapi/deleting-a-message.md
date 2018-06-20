---
title: メッセージを削除します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c8d46ac6f47eb4dc68aebfa4562403ef1b738213
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799895"
---
# <a name="deleting-a-message"></a><span data-ttu-id="30ddd-103">メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="30ddd-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="30ddd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30ddd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30ddd-105">クライアントが閉じていると、ユーザーがコンテンツのテーブルを表示するときに開いているし、ユーザーが読み取りまたはメッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="30ddd-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="30ddd-106">メッセージを誤って削除してからユーザーを保護するためには、MAPI は、2 段階の処理としてメッセージの削除を定義します。</span><span class="sxs-lookup"><span data-stu-id="30ddd-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="30ddd-107">削除済みアイテム フォルダーとして指定されているフォルダーに移動することによってメッセージに削除のマークを付ける: **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) のプロパティの識別子を持つエントリが格納されているフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="30ddd-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="30ddd-108">[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)メソッドを呼び出してメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="30ddd-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="30ddd-109">削除済みアイテム フォルダー以外のフォルダーにメッセージを削除するときに、削除対象としてマークします。</span><span class="sxs-lookup"><span data-stu-id="30ddd-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="30ddd-110">ユーザーが削除済みアイテム フォルダー内からメッセージを選択した場合にのみ、メッセージに物理的にから削除するかワークステーションです。</span><span class="sxs-lookup"><span data-stu-id="30ddd-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="30ddd-111">ユーザーが実際に削除を実行することを確認するプロンプトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="30ddd-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="30ddd-112">**メッセージを削除するのには**</span><span class="sxs-lookup"><span data-stu-id="30ddd-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="30ddd-113">ユーザーに間もなく削除は意図的なことを確認します。</span><span class="sxs-lookup"><span data-stu-id="30ddd-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="30ddd-114">削除するフォルダーの親を決定します。</span><span class="sxs-lookup"><span data-stu-id="30ddd-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="30ddd-115">削除済みアイテム フォルダーまたは削除済みアイテム フォルダー内にサブフォルダーがある場合は、メッセージを削除するのには[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="30ddd-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="30ddd-116">削除済みアイテム フォルダー内のフォルダーが含まれていない場合、は、メッセージを削除済みアイテム フォルダーに移動するのには、MESSAGE_MOVE フラグを設定して[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="30ddd-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

