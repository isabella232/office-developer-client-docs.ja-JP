---
title: テーブルの状態をダウンロードする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338340"
---
# <a name="download-table-state"></a><span data-ttu-id="a7df8-103">テーブルの状態をダウンロードする</span><span class="sxs-lookup"><span data-stu-id="a7df8-103">Download Table State</span></span>

  
  
<span data-ttu-id="a7df8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7df8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a7df8-105">このトピックでは、レプリケーションステート マシンのダウンロード テーブルの状態の間に何が起こるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="a7df8-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a7df8-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a7df8-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7df8-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="a7df8-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a7df8-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="a7df8-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="a7df8-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="a7df8-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="a7df8-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="a7df8-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="a7df8-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="a7df8-111">From this state:</span></span>  <br/> |[<span data-ttu-id="a7df8-112">コンテンツの状態を同期する</span><span class="sxs-lookup"><span data-stu-id="a7df8-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="a7df8-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="a7df8-113">To this state:</span></span>  <br/> |<span data-ttu-id="a7df8-114">コンテンツの状態を同期する</span><span class="sxs-lookup"><span data-stu-id="a7df8-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a7df8-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="a7df8-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a7df8-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7df8-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a7df8-117">説明</span><span class="sxs-lookup"><span data-stu-id="a7df8-117">Description</span></span>

<span data-ttu-id="a7df8-118">この状態では、フォルダーのダウンロードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="a7df8-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="a7df8-119">この状態の間、Outlookに関する情報を使用して、関連 **付けられた DNTBL** データ構造を初期化します。</span><span class="sxs-lookup"><span data-stu-id="a7df8-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="a7df8-120">クライアントはフォルダーの内容をダウンロードし、サーバーから新しいコンテンツ、変更、または削除を行ってローカル ストア上のフォルダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="a7df8-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="a7df8-121">ダウンロード プロセスでは、Microsoft Exchange増分変更同期 (ICS) が採用されます。</span><span class="sxs-lookup"><span data-stu-id="a7df8-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="a7df8-122">ICS の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7df8-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="a7df8-123">この状態が終了すると、ローカル ストアはコンテンツの同期状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="a7df8-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7df8-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="a7df8-124">See also</span></span>



[<span data-ttu-id="a7df8-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a7df8-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a7df8-126">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="a7df8-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a7df8-127">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="a7df8-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a7df8-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a7df8-128">SYNCSTATE</span></span>](syncstate.md)

