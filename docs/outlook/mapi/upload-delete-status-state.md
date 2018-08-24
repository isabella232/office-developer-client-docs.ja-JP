---
title: 削除状況アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4a45cfafec5126c72f365858e41963bc95fa707a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574546"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="1ad74-103">削除状況アップロード状態</span><span class="sxs-lookup"><span data-stu-id="1ad74-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="1ad74-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ad74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="1ad74-105">このトピックでは、アップロード削除状態マシンの状態、レプリケーション状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="1ad74-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1ad74-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1ad74-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ad74-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="1ad74-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="1ad74-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="1ad74-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="1ad74-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="1ad74-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="1ad74-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="1ad74-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="1ad74-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="1ad74-111">From this state:</span></span>  <br/> |[<span data-ttu-id="1ad74-112">テーブルの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="1ad74-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="1ad74-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="1ad74-113">To this state:</span></span>  <br/> |<span data-ttu-id="1ad74-114">テーブルの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="1ad74-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="1ad74-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="1ad74-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="1ad74-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ad74-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="1ad74-117">説明</span><span class="sxs-lookup"><span data-stu-id="1ad74-117">Description</span></span>

<span data-ttu-id="1ad74-118">この状態は、上記アップロード テーブルの状態で指定されたローカル ストア上のフォルダーで削除されている Outlook アイテム (メール、予定表、連絡先、タスク、メモ、または履歴) をサーバーに更新を開始します。</span><span class="sxs-lookup"><span data-stu-id="1ad74-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="1ad74-119">この状態は、中には、Outlook は、削除またはフォルダーから移動されたアイテムの情報が関連付けられている**UPDEL**データ構造体のメンバーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="1ad74-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="1ad74-120">クライアントは、サーバー上のフォルダーに指定した項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="1ad74-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="1ad74-121">削除済みではなく移動された項目を識別するためにクライアントは、 **UPDEL**構造体で指定された*pupmov*メンバーをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ad74-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="1ad74-122">この状態が終了すると Outlook はアイテムが削除されていることを示す内部情報を消去します。したがって、Outlook は、アイテムの記録です。</span><span class="sxs-lookup"><span data-stu-id="1ad74-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="1ad74-123">ローカル ストアは、アップロード ・ テーブルの状態を返します。</span><span class="sxs-lookup"><span data-stu-id="1ad74-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1ad74-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ad74-124">See also</span></span>



[<span data-ttu-id="1ad74-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="1ad74-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="1ad74-126">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="1ad74-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="1ad74-127">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="1ad74-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="1ad74-128">同期状態</span><span class="sxs-lookup"><span data-stu-id="1ad74-128">SYNCSTATE</span></span>](syncstate.md)

