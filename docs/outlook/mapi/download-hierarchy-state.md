---
title: 階層状態のダウンロード
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337010"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="e7395-103">階層状態のダウンロード</span><span class="sxs-lookup"><span data-stu-id="e7395-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="e7395-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7395-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e7395-105">このトピックでは、レプリケーションステートマシンのダウンロード階層状態の間に何が起こるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="e7395-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e7395-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e7395-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7395-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="e7395-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="e7395-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="e7395-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="e7395-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="e7395-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="e7395-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="e7395-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="e7395-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="e7395-111">From this state:</span></span>  <br/> |[<span data-ttu-id="e7395-112">同期状態</span><span class="sxs-lookup"><span data-stu-id="e7395-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="e7395-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="e7395-113">To this state:</span></span>  <br/> |<span data-ttu-id="e7395-114">同期状態</span><span class="sxs-lookup"><span data-stu-id="e7395-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e7395-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="e7395-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="e7395-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7395-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="e7395-117">説明</span><span class="sxs-lookup"><span data-stu-id="e7395-117">Description</span></span>

<span data-ttu-id="e7395-118">この状態では、サーバーからローカル ストアへのフォルダーのツリー階層のダウンロードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="e7395-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="e7395-119">Outlookへのポインターを使用して、**関連付けられた DNHIER** データ構造を初期化します。</span><span class="sxs-lookup"><span data-stu-id="e7395-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="e7395-120">クライアントは階層をダウンロードし、新しいフォルダーまたは変更をローカル ストア内のフォルダーに挿入します。</span><span class="sxs-lookup"><span data-stu-id="e7395-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="e7395-121">ダウンロード プロセスでは、Microsoft Exchange増分変更同期 (ICS) が採用されます。</span><span class="sxs-lookup"><span data-stu-id="e7395-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="e7395-122">ICS の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7395-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="e7395-123">この状態が終了すると、ローカル ストアは同期状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="e7395-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7395-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7395-124">See also</span></span>



[<span data-ttu-id="e7395-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="e7395-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e7395-126">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="e7395-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e7395-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="e7395-127">SYNCSTATE</span></span>](syncstate.md)

