---
title: 階層ダウンロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f9c334bc86bdff4abb2762642a37e3f0933a0b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589029"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="02fde-103">階層ダウンロード状態</span><span class="sxs-lookup"><span data-stu-id="02fde-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="02fde-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02fde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="02fde-105">ダウンロード階層マシンの状態、レプリケーション状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="02fde-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="02fde-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="02fde-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02fde-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="02fde-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="02fde-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="02fde-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="02fde-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="02fde-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="02fde-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="02fde-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="02fde-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="02fde-111">From this state:</span></span>  <br/> |[<span data-ttu-id="02fde-112">状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="02fde-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="02fde-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="02fde-113">To this state:</span></span>  <br/> |<span data-ttu-id="02fde-114">状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="02fde-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="02fde-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="02fde-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="02fde-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="02fde-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="02fde-117">説明</span><span class="sxs-lookup"><span data-stu-id="02fde-117">Description</span></span>

<span data-ttu-id="02fde-118">この状態は、ローカル ストアにフォルダーのツリー階層をサーバーからダウンロードを開始します。</span><span class="sxs-lookup"><span data-stu-id="02fde-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="02fde-119">Outlook では、階層構造へのポインターに関連付けられている**DNHIER**データ構造体を初期化します。</span><span class="sxs-lookup"><span data-stu-id="02fde-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="02fde-120">クライアントは、階層をダウンロードし、新しいフォルダーまたはフォルダーへの変更をローカル ストアに挿入します。。</span><span class="sxs-lookup"><span data-stu-id="02fde-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="02fde-121">ダウンロード処理では、Microsoft Exchange 増分変更の同期 (ICS) を適用します。</span><span class="sxs-lookup"><span data-stu-id="02fde-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="02fde-122">ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02fde-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="02fde-123">この状態が終了するとローカル ストアを同期の状態を返します。</span><span class="sxs-lookup"><span data-stu-id="02fde-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="02fde-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="02fde-124">See also</span></span>



[<span data-ttu-id="02fde-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="02fde-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="02fde-126">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="02fde-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="02fde-127">同期状態</span><span class="sxs-lookup"><span data-stu-id="02fde-127">SYNCSTATE</span></span>](syncstate.md)

