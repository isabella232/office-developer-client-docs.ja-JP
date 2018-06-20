---
title: ダウンロード メッセージ ヘッダーの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799951"
---
# <a name="download-message-header-state"></a><span data-ttu-id="070e2-103">ダウンロード メッセージ ヘッダーの状態</span><span class="sxs-lookup"><span data-stu-id="070e2-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="070e2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="070e2-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="070e2-105">このトピックでは、ダウンロード メッセージ ヘッダー マシンの状態、レプリケーション状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="070e2-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="070e2-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="070e2-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="070e2-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="070e2-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="070e2-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="070e2-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="070e2-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="070e2-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="070e2-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="070e2-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="070e2-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="070e2-111">From this state:</span></span>  <br/> |[<span data-ttu-id="070e2-112">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="070e2-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="070e2-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="070e2-113">To this state:</span></span>  <br/> |<span data-ttu-id="070e2-114">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="070e2-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="070e2-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="070e2-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="070e2-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="070e2-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="070e2-117">説明</span><span class="sxs-lookup"><span data-stu-id="070e2-117">Description</span></span>

<span data-ttu-id="070e2-118">この状態は、中には、クライアントは、ローカル ストアへのメッセージのヘッダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="070e2-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="070e2-119">ローカル ストアでは、 **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** 時にこの状態になるし、 **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** が呼び出されたときに終了します。</span><span class="sxs-lookup"><span data-stu-id="070e2-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="070e2-120">この状態は、中には、Outlook は、メッセージのヘッダーに関する情報を関連付けられている**HDRSYNC**データ構造体のメンバーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="070e2-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="070e2-121">クライアントでは、最初に完全なメッセージ項目をサーバーからダウンロードし、メッセージの項目をローカルでのヘッダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="070e2-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="070e2-122">同期が終了すると、クライアントは、ダウンロードの結果を設定します。</span><span class="sxs-lookup"><span data-stu-id="070e2-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="070e2-123">ローカル ストアは、アイドル状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="070e2-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="070e2-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="070e2-124">See also</span></span>



[<span data-ttu-id="070e2-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="070e2-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="070e2-126">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="070e2-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="070e2-127">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="070e2-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="070e2-128">同期状態</span><span class="sxs-lookup"><span data-stu-id="070e2-128">SYNCSTATE</span></span>](syncstate.md)

