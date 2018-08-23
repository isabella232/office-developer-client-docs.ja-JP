---
title: メッセージ アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 430734fe98799c386e71612355b194a6b8edf00a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575414"
---
# <a name="upload-message-state"></a><span data-ttu-id="2c034-103">メッセージ アップロード状態</span><span class="sxs-lookup"><span data-stu-id="2c034-103">Upload Message State</span></span>

  
  
<span data-ttu-id="2c034-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c034-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2c034-105">このトピックでは、アップロード メッセージの状態、レプリケーションの状態マシンの中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="2c034-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2c034-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2c034-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c034-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="2c034-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="2c034-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="2c034-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="2c034-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="2c034-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="2c034-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="2c034-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="2c034-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="2c034-111">From this state:</span></span>  <br/> |[<span data-ttu-id="2c034-112">テーブルの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="2c034-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="2c034-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="2c034-113">To this state:</span></span>  <br/> |<span data-ttu-id="2c034-114">テーブルの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="2c034-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="2c034-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="2c034-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="2c034-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c034-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="2c034-117">説明</span><span class="sxs-lookup"><span data-stu-id="2c034-117">Description</span></span>

<span data-ttu-id="2c034-118">この状態では、Outlook アイテム (メール、予定表、連絡先、タスク、メモ、または履歴) が変更されるかが新しいか、現在のフォルダーに移動されましたがアップロードを開始します。</span><span class="sxs-lookup"><span data-stu-id="2c034-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="2c034-119">追加、移動、または変更されると、outlook はアイテムの適切な情報を使用して correpsonding の**UPMSG**データ構造体を初期化します。</span><span class="sxs-lookup"><span data-stu-id="2c034-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="2c034-120">場合は、項目を追加または削除されたが、クライアント、適切に追加または、サーバー上の項目を更新します。</span><span class="sxs-lookup"><span data-stu-id="2c034-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="2c034-121">アイテムが変更された場合は、さらに、Outlook を指定**UPMSG**データ構造体に (である場合、アイテムがメッセージ ヘッダー) メッセージのヘッダー、アイテムのプロパティ、または競合を必要とするアイテムに変更をするかどうか解像度です。</span><span class="sxs-lookup"><span data-stu-id="2c034-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="2c034-122">クライアントは、サーバー上の項目を更新します。</span><span class="sxs-lookup"><span data-stu-id="2c034-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="2c034-123">アイテムのアップロードが終了すると Outlook メモ メッセージがアップロードされていることと、それ以降のアップロードでは処理されません。</span><span class="sxs-lookup"><span data-stu-id="2c034-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="2c034-124">ローカル ストアは、アップロード ・ テーブルの状態を返します。</span><span class="sxs-lookup"><span data-stu-id="2c034-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c034-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c034-125">See also</span></span>



[<span data-ttu-id="2c034-126">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="2c034-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2c034-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="2c034-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2c034-128">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="2c034-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2c034-129">同期状態</span><span class="sxs-lookup"><span data-stu-id="2c034-129">SYNCSTATE</span></span>](syncstate.md)

