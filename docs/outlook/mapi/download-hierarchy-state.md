---
title: 階層のダウンロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337010"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="2db10-103">階層のダウンロード状態</span><span class="sxs-lookup"><span data-stu-id="2db10-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="2db10-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2db10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2db10-105">このトピックでは、レプリケーション状態マシンのダウンロード階層状態中に行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="2db10-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2db10-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2db10-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2db10-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="2db10-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="2db10-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="2db10-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="2db10-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="2db10-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="2db10-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="2db10-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="2db10-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="2db10-111">From this state:</span></span>  <br/> |[<span data-ttu-id="2db10-112">同期状態</span><span class="sxs-lookup"><span data-stu-id="2db10-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="2db10-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="2db10-113">To this state:</span></span>  <br/> |<span data-ttu-id="2db10-114">同期状態</span><span class="sxs-lookup"><span data-stu-id="2db10-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="2db10-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="2db10-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="2db10-116">ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="2db10-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="2db10-117">説明</span><span class="sxs-lookup"><span data-stu-id="2db10-117">Description</span></span>

<span data-ttu-id="2db10-118">この状態によって、サーバーからローカルストアへのフォルダーのツリー階層のダウンロードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="2db10-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="2db10-119">Outlook は、関連付けられた**dnhier**データ構造を階層へのポインターで初期化します。</span><span class="sxs-lookup"><span data-stu-id="2db10-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="2db10-120">クライアントが階層をダウンロードし、新しいフォルダーまたは変更をローカルストア内のフォルダーに挿入します。</span><span class="sxs-lookup"><span data-stu-id="2db10-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="2db10-121">ダウンロードプロセスでは、Microsoft Exchange の増分変更の同期 (ICS) が採用されます。</span><span class="sxs-lookup"><span data-stu-id="2db10-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="2db10-122">ICS の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2db10-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="2db10-123">この状態が終了すると、ローカルストアは同期状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="2db10-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2db10-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2db10-124">See also</span></span>



[<span data-ttu-id="2db10-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="2db10-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2db10-126">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="2db10-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2db10-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="2db10-127">SYNCSTATE</span></span>](syncstate.md)

