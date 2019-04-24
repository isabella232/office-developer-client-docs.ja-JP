---
title: メッセージアップロードの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332635"
---
# <a name="upload-message-state"></a><span data-ttu-id="cde83-103">メッセージアップロードの状態</span><span class="sxs-lookup"><span data-stu-id="cde83-103">Upload Message State</span></span>

  
  
<span data-ttu-id="cde83-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cde83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="cde83-105">このトピックでは、レプリケーション状態マシンのメッセージ状態のアップロード中に行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="cde83-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="cde83-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="cde83-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cde83-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="cde83-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="cde83-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="cde83-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="cde83-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="cde83-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="cde83-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="cde83-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="cde83-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="cde83-111">From this state:</span></span>  <br/> |[<span data-ttu-id="cde83-112">テーブルの状態をアップロードする</span><span class="sxs-lookup"><span data-stu-id="cde83-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="cde83-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="cde83-113">To this state:</span></span>  <br/> |<span data-ttu-id="cde83-114">テーブルの状態をアップロードする</span><span class="sxs-lookup"><span data-stu-id="cde83-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="cde83-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="cde83-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="cde83-116">ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="cde83-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="cde83-117">説明</span><span class="sxs-lookup"><span data-stu-id="cde83-117">Description</span></span>

<span data-ttu-id="cde83-118">この状態では、Outlook アイテム (メール、予定表、連絡先、タスク、メモ、またはジャーナル) のアップロードが開始されます。これは、新規または現在のフォルダーに移動されたか、または変更されています。</span><span class="sxs-lookup"><span data-stu-id="cde83-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="cde83-119">Outlook は、アイテムが追加、移動、または変更されたときに、適切な情報を使用して correpsonding **upmsg**データ構造を初期化します。</span><span class="sxs-lookup"><span data-stu-id="cde83-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="cde83-120">アイテムが追加または移動された場合、クライアントはサーバー上のアイテムを適切に追加または更新します。</span><span class="sxs-lookup"><span data-stu-id="cde83-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="cde83-121">アイテムが変更されている場合、Outlook では、変更がメッセージヘッダー (場合にはメッセージヘッダー)、アイテムのプロパティ、またはアイテム自体で競合を必要とするかどうかについて、 **upmsg**データ構造でさらに指定します。画質.</span><span class="sxs-lookup"><span data-stu-id="cde83-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="cde83-122">クライアントは、サーバー上のアイテムを更新します。</span><span class="sxs-lookup"><span data-stu-id="cde83-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="cde83-123">アイテムのアップロードが終了すると、メッセージがアップロードされたことが Outlook によって記録されるので、以降のアップロードでは処理されません。</span><span class="sxs-lookup"><span data-stu-id="cde83-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="cde83-124">ローカルストアは、テーブルのアップロード状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="cde83-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cde83-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="cde83-125">See also</span></span>



[<span data-ttu-id="cde83-126">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="cde83-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="cde83-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="cde83-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="cde83-128">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="cde83-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="cde83-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="cde83-129">SYNCSTATE</span></span>](syncstate.md)

