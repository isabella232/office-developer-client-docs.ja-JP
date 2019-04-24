---
title: テーブルの状態をダウンロードする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338340"
---
# <a name="download-table-state"></a><span data-ttu-id="b5e14-103">テーブルの状態をダウンロードする</span><span class="sxs-lookup"><span data-stu-id="b5e14-103">Download Table State</span></span>

  
  
<span data-ttu-id="b5e14-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5e14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b5e14-105">このトピックでは、レプリケーション状態マシンのテーブルのダウンロード状態中に行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="b5e14-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b5e14-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b5e14-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5e14-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="b5e14-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b5e14-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="b5e14-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="b5e14-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="b5e14-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b5e14-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="b5e14-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="b5e14-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="b5e14-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b5e14-112">コンテンツの状態の同期</span><span class="sxs-lookup"><span data-stu-id="b5e14-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="b5e14-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="b5e14-113">To this state:</span></span>  <br/> |<span data-ttu-id="b5e14-114">コンテンツの状態の同期</span><span class="sxs-lookup"><span data-stu-id="b5e14-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b5e14-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="b5e14-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b5e14-116">ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5e14-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b5e14-117">説明</span><span class="sxs-lookup"><span data-stu-id="b5e14-117">Description</span></span>

<span data-ttu-id="b5e14-118">この状態では、フォルダーのダウンロードが開始します。</span><span class="sxs-lookup"><span data-stu-id="b5e14-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="b5e14-119">この状態の間、Outlook は、関連付けられた**dntbl**データ構造をフォルダーに関する情報で初期化します。</span><span class="sxs-lookup"><span data-stu-id="b5e14-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="b5e14-120">クライアントは、フォルダーの内容をダウンロードし、ローカルストアのフォルダーを新しい内容、変更、または削除をサーバーから更新します。</span><span class="sxs-lookup"><span data-stu-id="b5e14-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="b5e14-121">ダウンロードプロセスでは、Microsoft Exchange の増分変更の同期 (ICS) が採用されます。</span><span class="sxs-lookup"><span data-stu-id="b5e14-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="b5e14-122">ICS の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5e14-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="b5e14-123">この状態が終了すると、ローカルストアはコンテンツの同期状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="b5e14-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b5e14-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5e14-124">See also</span></span>



[<span data-ttu-id="b5e14-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="b5e14-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b5e14-126">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="b5e14-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b5e14-127">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="b5e14-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b5e14-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="b5e14-128">SYNCSTATE</span></span>](syncstate.md)

