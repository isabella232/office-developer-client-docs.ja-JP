---
title: メッセージヘッダーの状態をダウンロードする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338837"
---
# <a name="download-message-header-state"></a><span data-ttu-id="551c9-103">メッセージヘッダーの状態をダウンロードする</span><span class="sxs-lookup"><span data-stu-id="551c9-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="551c9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="551c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="551c9-105">このトピックでは、レプリケーション状態マシンのダウンロードメッセージヘッダーの状態中に行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="551c9-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="551c9-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="551c9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="551c9-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="551c9-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="551c9-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="551c9-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="551c9-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="551c9-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="551c9-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="551c9-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="551c9-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="551c9-111">From this state:</span></span>  <br/> |[<span data-ttu-id="551c9-112">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="551c9-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="551c9-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="551c9-113">To this state:</span></span>  <br/> |<span data-ttu-id="551c9-114">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="551c9-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="551c9-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="551c9-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="551c9-116">ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="551c9-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="551c9-117">説明</span><span class="sxs-lookup"><span data-stu-id="551c9-117">Description</span></span>

<span data-ttu-id="551c9-118">この状態の間、クライアントはローカルストアのメッセージのヘッダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="551c9-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="551c9-119">iostx:: **[SyncHdrEnd](iostx-synchdrend.md)** が呼び出されると、ローカルストアはこの状態になります。 **[iostx:: SyncHdrBeg](iostx-synchdrbeg.md)** と終了します。</span><span class="sxs-lookup"><span data-stu-id="551c9-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="551c9-120">この状態の間、Outlook は、関連付けられた**HDRSYNC**データ構造のメンバーを、メッセージのヘッダーに関する情報を使用して初期化します。</span><span class="sxs-lookup"><span data-stu-id="551c9-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="551c9-121">クライアントはまず、サーバーからメッセージアイテム全体をダウンロードしてから、メッセージアイテムのヘッダーをローカルに更新します。</span><span class="sxs-lookup"><span data-stu-id="551c9-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="551c9-122">同期が終了すると、クライアントはダウンロード結果を設定します。</span><span class="sxs-lookup"><span data-stu-id="551c9-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="551c9-123">ローカルストアは、アイドル状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="551c9-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="551c9-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="551c9-124">See also</span></span>



[<span data-ttu-id="551c9-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="551c9-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="551c9-126">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="551c9-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="551c9-127">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="551c9-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="551c9-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="551c9-128">SYNCSTATE</span></span>](syncstate.md)

