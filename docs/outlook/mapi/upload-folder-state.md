---
title: フォルダーの状態をアップロードする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348427"
---
# <a name="upload-folder-state"></a><span data-ttu-id="2b533-103">フォルダーの状態をアップロードする</span><span class="sxs-lookup"><span data-stu-id="2b533-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="2b533-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b533-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2b533-105">このトピックでは、レプリケーション状態マシンのアップロードフォルダーの状態中に行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="2b533-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2b533-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2b533-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b533-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="2b533-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="2b533-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="2b533-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="2b533-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="2b533-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="2b533-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="2b533-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="2b533-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="2b533-111">From this state:</span></span>  <br/> |[<span data-ttu-id="2b533-112">階層のアップロード状態</span><span class="sxs-lookup"><span data-stu-id="2b533-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="2b533-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="2b533-113">To this state:</span></span>  <br/> |<span data-ttu-id="2b533-114">階層のアップロード状態</span><span class="sxs-lookup"><span data-stu-id="2b533-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="2b533-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="2b533-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="2b533-116">ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b533-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="2b533-117">説明</span><span class="sxs-lookup"><span data-stu-id="2b533-117">Description</span></span>

<span data-ttu-id="2b533-118">この状態では、上記のアップロード階層の状態で指定された階層内のフォルダーのアップロードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="2b533-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="2b533-119">この状態では、Outlook はフォルダーオブジェクト (削除されていない場合) とフォルダーの状態 (新規、移動、変更、または削除) が対応する**UPFLD**データ構造の一部として指定されていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="2b533-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="2b533-120">クライアントは、この情報をサーバーにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="2b533-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="2b533-121">アップロードが成功すると、クライアントは**UPFLD**の*ulflags*を**UPF_OK**に設定します。</span><span class="sxs-lookup"><span data-stu-id="2b533-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="2b533-122">その後、Outlook は、フォルダーをアップロードする要求に関する内部情報をクリアします。</span><span class="sxs-lookup"><span data-stu-id="2b533-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="2b533-123">フォルダーのアップロードが終了すると、ローカルストアはアップロード階層の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="2b533-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="2b533-124">前述のアップロード階層の状態に対応する**[uphier](uphier.md)** 構造に基づいて、Outlook は次のフォルダーのアップロードを続行するかどうかを決定し、次のアップロードフォルダーの状態を準備します。</span><span class="sxs-lookup"><span data-stu-id="2b533-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2b533-125">クライアントが1つのフォルダーのみをアップロードする必要がある場合、クライアントは、階層のアップロード状態を入力せずに[同期状態](synchronize-state.md)でレプリケーションを開始できます。</span><span class="sxs-lookup"><span data-stu-id="2b533-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="2b533-126">クライアントは、 **[SYNC](sync.md)** *フラグ*を**UPS_UPLOAD_ONLY**および**UPS_ONE_FOLDER**および*feid*にフォルダーの id に設定することによって、1つのフォルダーのみがアップロードされるように Outlook に指示します。</span><span class="sxs-lookup"><span data-stu-id="2b533-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b533-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b533-127">See also</span></span>



[<span data-ttu-id="2b533-128">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="2b533-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2b533-129">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="2b533-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2b533-130">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="2b533-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2b533-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="2b533-131">SYNCSTATE</span></span>](syncstate.md)

