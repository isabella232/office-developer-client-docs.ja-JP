---
title: アップロード ステータスのステートを削除
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ff957e649d5de64c65ac169b3bc413ac7b6c9491
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804180"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="e3fb6-103">アップロード ステータスのステートを削除</span><span class="sxs-lookup"><span data-stu-id="e3fb6-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="e3fb6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3fb6-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="e3fb6-105">このトピックでは、アップロード削除状態マシンの状態、レプリケーション状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e3fb6-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e3fb6-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3fb6-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="e3fb6-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="e3fb6-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="e3fb6-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="e3fb6-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="e3fb6-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="e3fb6-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-111">From this state:</span></span>  <br/> |[<span data-ttu-id="e3fb6-112">テーブルの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="e3fb6-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-113">To this state:</span></span>  <br/> |<span data-ttu-id="e3fb6-114">テーブルの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e3fb6-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="e3fb6-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="e3fb6-117">説明</span><span class="sxs-lookup"><span data-stu-id="e3fb6-117">Description</span></span>

<span data-ttu-id="e3fb6-118">この状態は、上記アップロード テーブルの状態で指定されたローカル ストア上のフォルダーで削除されている Outlook アイテム (メール、予定表、連絡先、タスク、メモ、または履歴) をサーバーに更新を開始します。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="e3fb6-119">この状態は、中には、Outlook は、削除またはフォルダーから移動されたアイテムの情報が関連付けられている**UPDEL**データ構造体のメンバーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="e3fb6-120">クライアントは、サーバー上のフォルダーに指定した項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="e3fb6-121">削除済みではなく移動された項目を識別するためにクライアントは、 **UPDEL**構造体で指定された*pupmov*メンバーをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="e3fb6-122">この状態が終了すると Outlook はアイテムが削除されていることを示す内部情報を消去します。したがって、Outlook は、アイテムの記録です。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="e3fb6-123">ローカル ストアは、アップロード ・ テーブルの状態を返します。</span><span class="sxs-lookup"><span data-stu-id="e3fb6-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e3fb6-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3fb6-124">See also</span></span>



[<span data-ttu-id="e3fb6-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="e3fb6-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e3fb6-126">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="e3fb6-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e3fb6-127">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="e3fb6-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e3fb6-128">同期状態</span><span class="sxs-lookup"><span data-stu-id="e3fb6-128">SYNCSTATE</span></span>](syncstate.md)

