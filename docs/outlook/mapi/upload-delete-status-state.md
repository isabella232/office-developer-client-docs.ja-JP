---
title: アップロード状態の削除
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425842"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="4287a-103">アップロード状態の削除</span><span class="sxs-lookup"><span data-stu-id="4287a-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="4287a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4287a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4287a-105">このトピックでは、レプリケーションステート マシンのアップロード削除状態の間に発生する処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="4287a-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4287a-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="4287a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4287a-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="4287a-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4287a-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="4287a-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="4287a-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="4287a-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4287a-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="4287a-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="4287a-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="4287a-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4287a-112">アップロード状態</span><span class="sxs-lookup"><span data-stu-id="4287a-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="4287a-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="4287a-113">To this state:</span></span>  <br/> |<span data-ttu-id="4287a-114">アップロード状態</span><span class="sxs-lookup"><span data-stu-id="4287a-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4287a-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="4287a-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4287a-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="4287a-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4287a-117">説明</span><span class="sxs-lookup"><span data-stu-id="4287a-117">Description</span></span>

<span data-ttu-id="4287a-118">この状態は、前のアップロード テーブルの状態で指定されたローカル ストアのフォルダー内で削除された Outlook アイテム (メール、予定表、連絡先、タスク、メモ、またはジャーナル) の更新をサーバーで開始します。</span><span class="sxs-lookup"><span data-stu-id="4287a-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="4287a-119">この状態の間Outlook、フォルダーから削除または移動されたアイテムの情報を使用して、関連付けられた **UPDEL** データ構造のメンバーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="4287a-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="4287a-120">その後、クライアントはサーバー上のフォルダー内の指定されたアイテムを削除します。</span><span class="sxs-lookup"><span data-stu-id="4287a-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="4287a-121">削除されたのではなく移動されたアイテムを区別するには、UPDEL 構造で識別された  *pupmov*  メンバーをクライアントが **チェックする必要** があります。</span><span class="sxs-lookup"><span data-stu-id="4287a-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="4287a-122">この状態が終了するとOutlookアイテムが削除されたことを示す内部情報が消去されます。したがって、Outlookアイテムのレコードが存在しなくなりました。</span><span class="sxs-lookup"><span data-stu-id="4287a-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="4287a-123">ローカル ストアは、アップロード テーブルの状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="4287a-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4287a-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="4287a-124">See also</span></span>



[<span data-ttu-id="4287a-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="4287a-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4287a-126">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="4287a-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4287a-127">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="4287a-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4287a-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4287a-128">SYNCSTATE</span></span>](syncstate.md)

