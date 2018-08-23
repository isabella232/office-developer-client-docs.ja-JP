---
title: テーブル アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bd54c30e8701a13637235e28ddcfef4c21d10a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576982"
---
# <a name="upload-table-state"></a><span data-ttu-id="48134-103">テーブル アップロード状態</span><span class="sxs-lookup"><span data-stu-id="48134-103">Upload Table State</span></span>

  
  
<span data-ttu-id="48134-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48134-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="48134-105">このトピックでは、アップロード テーブル マシンの状態、レプリケーション状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="48134-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="48134-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="48134-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48134-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="48134-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="48134-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="48134-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="48134-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="48134-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="48134-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="48134-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="48134-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="48134-111">From this state:</span></span>  <br/> |[<span data-ttu-id="48134-112">内容の状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="48134-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="48134-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="48134-113">To this state:</span></span>  <br/> |<span data-ttu-id="48134-114">[メッセージの状態をアップロード](upload-message-state.md)[アップロードの状態の状態の削除](upload-delete-status-state.md)、[アップロードのステータスの状態を読み取り](upload-read-status-state.md)、内容の状態を同期または</span><span class="sxs-lookup"><span data-stu-id="48134-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="48134-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="48134-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="48134-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="48134-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="48134-117">説明</span><span class="sxs-lookup"><span data-stu-id="48134-117">Description</span></span>

<span data-ttu-id="48134-118">この状態は、上記同期コンテンツの状態で指定されたフォルダーの内容をアップロードを開始します。</span><span class="sxs-lookup"><span data-stu-id="48134-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="48134-119">フォルダーは、メール、予定表、連絡先、仕事、メモ、または履歴のフォルダーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="48134-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="48134-120">この状態は、中に Outlook が追加、変更、移動、削除、または読み取りとしてマークされている項目のリストを作成し、対応するアップロード メッセージの状態の適切な内部情報を準備して、アップロード ステータスの状態を削除するか、アップロード ステータスの読み取り状態です。</span><span class="sxs-lookup"><span data-stu-id="48134-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="48134-121">この状態が終了すると、Outlook は、コンテンツがアップロードされないようにするもう一度別の変更が行われるまで、同期するには、その内容を持つものとしてフォルダーをマークします。</span><span class="sxs-lookup"><span data-stu-id="48134-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="48134-122">ローカル ストアは、コンテンツの同期の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="48134-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="48134-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="48134-123">See also</span></span>



[<span data-ttu-id="48134-124">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="48134-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="48134-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="48134-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="48134-126">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="48134-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="48134-127">同期状態</span><span class="sxs-lookup"><span data-stu-id="48134-127">SYNCSTATE</span></span>](syncstate.md)

