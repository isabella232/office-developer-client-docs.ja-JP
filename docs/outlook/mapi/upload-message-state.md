---
title: アップロードメッセージの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433802"
---
# <a name="upload-message-state"></a><span data-ttu-id="38f76-103">アップロードメッセージの状態</span><span class="sxs-lookup"><span data-stu-id="38f76-103">Upload Message State</span></span>

  
  
<span data-ttu-id="38f76-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38f76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="38f76-105">このトピックでは、レプリケーションステート マシンのアップロード メッセージの状態の間に発生する処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="38f76-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="38f76-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="38f76-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38f76-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="38f76-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="38f76-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="38f76-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="38f76-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="38f76-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="38f76-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="38f76-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="38f76-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="38f76-111">From this state:</span></span>  <br/> |[<span data-ttu-id="38f76-112">アップロード状態</span><span class="sxs-lookup"><span data-stu-id="38f76-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="38f76-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="38f76-113">To this state:</span></span>  <br/> |<span data-ttu-id="38f76-114">アップロード状態</span><span class="sxs-lookup"><span data-stu-id="38f76-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="38f76-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="38f76-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="38f76-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="38f76-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="38f76-117">説明</span><span class="sxs-lookup"><span data-stu-id="38f76-117">Description</span></span>

<span data-ttu-id="38f76-118">この状態は、Outlook アイテム (メール、予定表、連絡先、タスク、メモ、またはジャーナル) のアップロードを開始します。新しいアイテム、または現在のフォルダーに移動されたアイテム、または変更されたアイテム。</span><span class="sxs-lookup"><span data-stu-id="38f76-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="38f76-119">Outlook、追加、移動、または変更されるアイテムの適切な情報を使用して、correpsonding **UPMSG** データ構造を初期化します。</span><span class="sxs-lookup"><span data-stu-id="38f76-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="38f76-120">アイテムが追加または移動された場合、クライアントはサーバー上のアイテムを適切に追加または更新します。</span><span class="sxs-lookup"><span data-stu-id="38f76-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="38f76-121">アイテムが変更されている場合、Outlook は **UPMSG** データ構造で、変更がメッセージ ヘッダー (この場合はメッセージ ヘッダー)、アイテム プロパティ、または競合解決が必要なアイテム自体に含まれるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="38f76-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="38f76-122">その後、クライアントはサーバー上のアイテムを更新します。</span><span class="sxs-lookup"><span data-stu-id="38f76-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="38f76-123">アイテムのアップロードが終了するとOutlookメッセージがアップロードされたというメモが表示され、後続のアップロードでは処理されません。</span><span class="sxs-lookup"><span data-stu-id="38f76-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="38f76-124">ローカル ストアは、アップロード テーブルの状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="38f76-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="38f76-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="38f76-125">See also</span></span>



[<span data-ttu-id="38f76-126">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="38f76-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="38f76-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="38f76-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="38f76-128">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="38f76-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="38f76-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="38f76-129">SYNCSTATE</span></span>](syncstate.md)

