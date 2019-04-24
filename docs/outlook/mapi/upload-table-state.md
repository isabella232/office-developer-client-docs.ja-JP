---
title: テーブルの状態をアップロードする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342841"
---
# <a name="upload-table-state"></a><span data-ttu-id="2f2b1-103">テーブルの状態をアップロードする</span><span class="sxs-lookup"><span data-stu-id="2f2b1-103">Upload Table State</span></span>

  
  
<span data-ttu-id="2f2b1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f2b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2f2b1-105">このトピックでは、レプリケーション状態マシンのテーブル状態のアップロード中に行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2f2b1-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2f2b1-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f2b1-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="2f2b1-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="2f2b1-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="2f2b1-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="2f2b1-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="2f2b1-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="2f2b1-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="2f2b1-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="2f2b1-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="2f2b1-111">From this state:</span></span>  <br/> |[<span data-ttu-id="2f2b1-112">コンテンツの状態の同期</span><span class="sxs-lookup"><span data-stu-id="2f2b1-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="2f2b1-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="2f2b1-113">To this state:</span></span>  <br/> |<span data-ttu-id="2f2b1-114">[メッセージの状態のアップロード](upload-message-state.md)、削除の状態の[状態](upload-delete-status-state.md)のアップロード、[読み取り状態のアップロード](upload-read-status-state.md)、またはコンテンツの状態の同期</span><span class="sxs-lookup"><span data-stu-id="2f2b1-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="2f2b1-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="2f2b1-116">ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="2f2b1-117">説明</span><span class="sxs-lookup"><span data-stu-id="2f2b1-117">Description</span></span>

<span data-ttu-id="2f2b1-118">この状態では、以前のコンテンツ同期状態で指定されたフォルダーのコンテンツのアップロードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="2f2b1-119">このフォルダーは、メール、予定表、連絡先、タスク、メモ、または履歴フォルダーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="2f2b1-120">この状態では、Outlook によって、追加、変更、移動、削除、または開封済みとしてマークされたアイテムの一覧が作成され、対応するアップロードメッセージの状態のアップロード、削除の状態の確認、または読み取り状態のアップロードのための適切な内部情報を準備します。ステータス.</span><span class="sxs-lookup"><span data-stu-id="2f2b1-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="2f2b1-121">この状態が終了すると、Outlook はフォルダーにコンテンツが同期されているというマークを付けます。これにより、別の変更が行われるまで内容が再度アップロードされることはありません。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="2f2b1-122">ローカルストアは、コンテンツの同期状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f2b1-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f2b1-123">See also</span></span>



[<span data-ttu-id="2f2b1-124">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="2f2b1-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2f2b1-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="2f2b1-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2f2b1-126">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="2f2b1-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2f2b1-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="2f2b1-127">SYNCSTATE</span></span>](syncstate.md)

