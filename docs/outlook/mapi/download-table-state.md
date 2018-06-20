---
title: ダウンロード ・ テーブルの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6a29cc131b4fe352b067e343376b2b705e8e3244
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799973"
---
# <a name="download-table-state"></a><span data-ttu-id="0bd89-103">ダウンロード ・ テーブルの状態</span><span class="sxs-lookup"><span data-stu-id="0bd89-103">Download Table State</span></span>

  
  
<span data-ttu-id="0bd89-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0bd89-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="0bd89-105">ダウンロード テーブル マシンの状態、レプリケーション状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="0bd89-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0bd89-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="0bd89-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0bd89-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="0bd89-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="0bd89-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="0bd89-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="0bd89-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="0bd89-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="0bd89-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="0bd89-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="0bd89-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="0bd89-111">From this state:</span></span>  <br/> |[<span data-ttu-id="0bd89-112">内容の状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="0bd89-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="0bd89-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="0bd89-113">To this state:</span></span>  <br/> |<span data-ttu-id="0bd89-114">内容の状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="0bd89-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="0bd89-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="0bd89-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="0bd89-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bd89-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="0bd89-117">説明</span><span class="sxs-lookup"><span data-stu-id="0bd89-117">Description</span></span>

<span data-ttu-id="0bd89-118">この状態は、フォルダーのダウンロードを開始します。</span><span class="sxs-lookup"><span data-stu-id="0bd89-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="0bd89-119">この状態は、中には、Outlook は、フォルダーに関する情報が関連付けられている**DNTBL**データ構造体を初期化します。</span><span class="sxs-lookup"><span data-stu-id="0bd89-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="0bd89-120">クライアントは、フォルダーの内容をダウンロードし、新しい内容、変更、またはサーバーからの削除を使用してローカル ストア上のフォルダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="0bd89-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="0bd89-121">ダウンロード処理では、Microsoft Exchange 増分変更の同期 (ICS) を適用します。</span><span class="sxs-lookup"><span data-stu-id="0bd89-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="0bd89-122">ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bd89-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="0bd89-123">この状態が終了するとローカル ストアを同期化コンテンツの状態を返します。</span><span class="sxs-lookup"><span data-stu-id="0bd89-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0bd89-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="0bd89-124">See also</span></span>



[<span data-ttu-id="0bd89-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="0bd89-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="0bd89-126">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="0bd89-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="0bd89-127">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="0bd89-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="0bd89-128">同期状態</span><span class="sxs-lookup"><span data-stu-id="0bd89-128">SYNCSTATE</span></span>](syncstate.md)

