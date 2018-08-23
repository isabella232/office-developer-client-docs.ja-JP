---
title: フォルダー アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ae8c3c4012874e1ca35761b103066cceebb1b165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576751"
---
# <a name="upload-folder-state"></a><span data-ttu-id="ede70-103">フォルダー アップロード状態</span><span class="sxs-lookup"><span data-stu-id="ede70-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="ede70-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ede70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ede70-105">アップロード フォルダー マシンの状態、レプリケーション状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="ede70-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ede70-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ede70-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ede70-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="ede70-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="ede70-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="ede70-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="ede70-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="ede70-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="ede70-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="ede70-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="ede70-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="ede70-111">From this state:</span></span>  <br/> |[<span data-ttu-id="ede70-112">階層の状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="ede70-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="ede70-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="ede70-113">To this state:</span></span>  <br/> |<span data-ttu-id="ede70-114">階層の状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="ede70-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="ede70-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="ede70-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="ede70-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ede70-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="ede70-117">説明</span><span class="sxs-lookup"><span data-stu-id="ede70-117">Description</span></span>

<span data-ttu-id="ede70-118">この状態は、上記のアップロードの階層状態で指定された階層内のフォルダーをアップロードを開始します。</span><span class="sxs-lookup"><span data-stu-id="ede70-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="ede70-119">この状態は、中には、Outlook は、(削除されていない) 場合は、フォルダー オブジェクトおよび対応する**UPFLD**のデータ構造の一部としてフォルダー (新規作成、移動、変更、または削除) の状態を示すフラグを提供します。</span><span class="sxs-lookup"><span data-stu-id="ede70-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="ede70-120">クライアントは、この情報をサーバーにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="ede70-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="ede70-121">アップロードが成功した場合、クライアントは、 **UPF_OK**に**UPFLD**で*ulFlags*を設定します。</span><span class="sxs-lookup"><span data-stu-id="ede70-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="ede70-122">Outlook は、フォルダーをアップロードする要求に関する内部情報を消去します。</span><span class="sxs-lookup"><span data-stu-id="ede70-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="ede70-123">フォルダーのアップロードが終了すると、ローカル ストアは、アップロード階層状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="ede70-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="ede70-124">Outlook は上記のアップロードの階層の状態に対応する**[UPHIER](uphier.md)** 構造に基づく、および次のアップロード フォルダーの状態を準備するのには次のフォルダーのアップロードを続行するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ede70-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ede70-125">クライアントは、1 つのフォルダーをアップロードする必要がある、クライアントは、アップロードの階層の状態を入力することがなく[状態の同期](synchronize-state.md)を使用する、レプリケーションを開始できます。</span><span class="sxs-lookup"><span data-stu-id="ede70-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="ede70-126">クライアントが特定のメンバーとの**[同期](sync.md)** を設定- **UPS_UPLOAD_ONLY** 、 **UPS_ONE_FOLDER**およびフォルダーの ID を*feid*に*ulFlags* -アップロードは 1 つだけフォルダーを Outlook に通知します。</span><span class="sxs-lookup"><span data-stu-id="ede70-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ede70-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="ede70-127">See also</span></span>



[<span data-ttu-id="ede70-128">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="ede70-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ede70-129">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="ede70-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ede70-130">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="ede70-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ede70-131">同期状態</span><span class="sxs-lookup"><span data-stu-id="ede70-131">SYNCSTATE</span></span>](syncstate.md)

