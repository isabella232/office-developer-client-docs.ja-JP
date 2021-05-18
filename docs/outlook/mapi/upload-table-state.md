---
title: アップロードテーブルの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405822"
---
# <a name="upload-table-state"></a><span data-ttu-id="7b4b2-103">アップロードテーブルの状態</span><span class="sxs-lookup"><span data-stu-id="7b4b2-103">Upload Table State</span></span>

  
  
<span data-ttu-id="7b4b2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b4b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7b4b2-105">このトピックでは、レプリケーションステート マシンのアップロード テーブルの状態の間に何が起こるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="7b4b2-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7b4b2-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="7b4b2-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b4b2-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="7b4b2-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="7b4b2-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="7b4b2-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="7b4b2-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="7b4b2-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="7b4b2-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="7b4b2-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="7b4b2-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="7b4b2-111">From this state:</span></span>  <br/> |[<span data-ttu-id="7b4b2-112">コンテンツの状態を同期する</span><span class="sxs-lookup"><span data-stu-id="7b4b2-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="7b4b2-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="7b4b2-113">To this state:</span></span>  <br/> |<span data-ttu-id="7b4b2-114">[アップロード状態、](upload-message-state.md)[削除状態のアップロード、](upload-delete-status-state.md)読み取[](upload-read-status-state.md)り状態のアップロード、コンテンツの状態の同期</span><span class="sxs-lookup"><span data-stu-id="7b4b2-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="7b4b2-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="7b4b2-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="7b4b2-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b4b2-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="7b4b2-117">説明</span><span class="sxs-lookup"><span data-stu-id="7b4b2-117">Description</span></span>

<span data-ttu-id="7b4b2-118">この状態では、前の同期コンテンツ状態で指定されたフォルダーのコンテンツのアップロードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="7b4b2-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="7b4b2-119">フォルダーには、メール、予定表、連絡先、タスク、メモ、またはジャーナル フォルダーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7b4b2-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="7b4b2-120">この状態の間、Outlook は、追加、変更、移動、削除、または読み取りとしてマークされたアイテムのリストを作成し、対応するアップロード メッセージの状態、削除状態のアップロード、または読み取り状態のアップロードに関する適切な内部情報を準備します。</span><span class="sxs-lookup"><span data-stu-id="7b4b2-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="7b4b2-121">この状態が終了すると、Outlookが同期されたフォルダーとしてマークされ、別の変更が行われたまでコンテンツが再びアップロードされません。</span><span class="sxs-lookup"><span data-stu-id="7b4b2-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="7b4b2-122">ローカル ストアは、コンテンツの同期状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="7b4b2-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b4b2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b4b2-123">See also</span></span>



[<span data-ttu-id="7b4b2-124">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="7b4b2-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7b4b2-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="7b4b2-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="7b4b2-126">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="7b4b2-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7b4b2-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="7b4b2-127">SYNCSTATE</span></span>](syncstate.md)

