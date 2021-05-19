---
title: アップロードフォルダーの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419570"
---
# <a name="upload-folder-state"></a><span data-ttu-id="070f7-103">アップロードフォルダーの状態</span><span class="sxs-lookup"><span data-stu-id="070f7-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="070f7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="070f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="070f7-105">このトピックでは、レプリケーション状態マシンのアップロード フォルダーの状態の間に何が起こるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="070f7-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="070f7-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="070f7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="070f7-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="070f7-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="070f7-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="070f7-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="070f7-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="070f7-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="070f7-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="070f7-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="070f7-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="070f7-111">From this state:</span></span>  <br/> |[<span data-ttu-id="070f7-112">アップロード階層の状態</span><span class="sxs-lookup"><span data-stu-id="070f7-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="070f7-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="070f7-113">To this state:</span></span>  <br/> |<span data-ttu-id="070f7-114">アップロード階層の状態</span><span class="sxs-lookup"><span data-stu-id="070f7-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="070f7-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="070f7-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="070f7-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="070f7-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="070f7-117">説明</span><span class="sxs-lookup"><span data-stu-id="070f7-117">Description</span></span>

<span data-ttu-id="070f7-118">この状態では、前のアップロード階層状態で指定された階層内のフォルダーのアップロードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="070f7-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="070f7-119">この状態の間、Outlook はフォルダー オブジェクト (削除されていない場合) と、対応する **UPFLD** データ構造の一部としてフォルダーの状態 (新規、移動、変更、または削除) を示すフラグを提供します。</span><span class="sxs-lookup"><span data-stu-id="070f7-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="070f7-120">クライアントは、この情報をサーバーにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="070f7-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="070f7-121">アップロードが成功した場合、クライアントは *UPFLD の ulFlags* を **UPF_OK。** </span><span class="sxs-lookup"><span data-stu-id="070f7-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="070f7-122">Outlookをアップロードする要求に関する内部情報をクリアします。</span><span class="sxs-lookup"><span data-stu-id="070f7-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="070f7-123">フォルダーのアップロードが終了すると、ローカル ストアはアップロード階層の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="070f7-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="070f7-124">前のアップロード階層状態に対応する **[UPHIER](uphier.md)** 構造に基づいて、Outlook は次のフォルダーのアップロードを続行し、次のアップロード フォルダーの状態に備えるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="070f7-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="070f7-125">クライアントが 1 つのフォルダーのみをアップロードする必要がある場合、クライアントはアップロード[](synchronize-state.md)階層状態に入ることなく同期状態を使用してレプリケーションを開始できます。</span><span class="sxs-lookup"><span data-stu-id="070f7-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="070f7-126">クライアントは、SYNC の **[](sync.md)** 特定のメンバー *(ulFlags)* を **UPS_UPLOAD_ONLY** と **UPS_ONE_FOLDER** に設定し、フォルダーの ID に *feid* を設定して、Outlook に 1 つのフォルダーだけがアップロードされるというメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="070f7-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="070f7-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="070f7-127">See also</span></span>



[<span data-ttu-id="070f7-128">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="070f7-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="070f7-129">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="070f7-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="070f7-130">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="070f7-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="070f7-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="070f7-131">SYNCSTATE</span></span>](syncstate.md)

