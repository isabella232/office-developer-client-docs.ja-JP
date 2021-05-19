---
title: メッセージ ヘッダーの状態のダウンロード
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417120"
---
# <a name="download-message-header-state"></a><span data-ttu-id="ca98f-103">メッセージ ヘッダーの状態のダウンロード</span><span class="sxs-lookup"><span data-stu-id="ca98f-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="ca98f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca98f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ca98f-105">このトピックでは、レプリケーション状態マシンのダウンロード メッセージ ヘッダー状態の間に何が起こるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="ca98f-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ca98f-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ca98f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca98f-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="ca98f-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="ca98f-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="ca98f-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="ca98f-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="ca98f-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="ca98f-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="ca98f-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="ca98f-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="ca98f-111">From this state:</span></span>  <br/> |[<span data-ttu-id="ca98f-112">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="ca98f-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="ca98f-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="ca98f-113">To this state:</span></span>  <br/> |<span data-ttu-id="ca98f-114">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="ca98f-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="ca98f-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="ca98f-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="ca98f-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca98f-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="ca98f-117">説明</span><span class="sxs-lookup"><span data-stu-id="ca98f-117">Description</span></span>

<span data-ttu-id="ca98f-118">この状態の間、クライアントはローカル ストア上のメッセージのヘッダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="ca98f-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="ca98f-119">ローカル ストアは **[、IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** にこの状態を入力し **[、IOSTX::SyncHdrEnd](iostx-synchdrend.md)** が呼び出された場合に終了します。</span><span class="sxs-lookup"><span data-stu-id="ca98f-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="ca98f-120">この状態の間Outlook、関連付けられた **HDRSYNC** データ構造のメンバーを、メッセージのヘッダーに関する情報で初期化します。</span><span class="sxs-lookup"><span data-stu-id="ca98f-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="ca98f-121">クライアントは、最初にサーバーから完全なメッセージ アイテムをダウンロードし、メッセージ アイテムのヘッダーをローカルで更新します。</span><span class="sxs-lookup"><span data-stu-id="ca98f-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="ca98f-122">同期が終了すると、クライアントはダウンロード結果を設定します。</span><span class="sxs-lookup"><span data-stu-id="ca98f-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="ca98f-123">ローカル ストアはアイドル状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="ca98f-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca98f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca98f-124">See also</span></span>



[<span data-ttu-id="ca98f-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="ca98f-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ca98f-126">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="ca98f-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ca98f-127">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="ca98f-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ca98f-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="ca98f-128">SYNCSTATE</span></span>](syncstate.md)

