---
title: 同期状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349512"
---
# <a name="synchronize-state"></a><span data-ttu-id="92611-103">同期状態</span><span class="sxs-lookup"><span data-stu-id="92611-103">Synchronize State</span></span>

  
  
<span data-ttu-id="92611-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92611-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="92611-105">このトピックでは、レプリケーション状態マシンの同期状態中に行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="92611-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="92611-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="92611-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92611-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="92611-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="92611-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="92611-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="92611-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="92611-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="92611-110">**[頻度](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="92611-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="92611-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="92611-111">From this state:</span></span>  <br/> |[<span data-ttu-id="92611-112">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="92611-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="92611-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="92611-113">To this state:</span></span>  <br/> |<span data-ttu-id="92611-114">[階層の状態をダウンロード](download-hierarchy-state.md)する、[コンテンツの状態を同期](synchronize-contents-state.md)する、階層の[アップロード状態](upload-hierarchy-state.md)、またはアイドル状態</span><span class="sxs-lookup"><span data-stu-id="92611-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="92611-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="92611-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="92611-116">ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="92611-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="92611-117">説明</span><span class="sxs-lookup"><span data-stu-id="92611-117">Description</span></span>

<span data-ttu-id="92611-118">この状態は、同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="92611-118">This state initiates synchronization.</span></span> <span data-ttu-id="92611-119">ローカルストアは、ここからアップロードまたはダウンロード状態に移行できます。</span><span class="sxs-lookup"><span data-stu-id="92611-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="92611-120">たとえば、ローカルストアは、アップロード階層状態に移動してフォルダー階層をサーバーにアップロードすることも、最初に階層をアップロードしてから階層をサーバーからダウンロードして、完全同期を実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="92611-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="92611-121">この状態の間、outlook は関連する**同期**データ構造をローカルストアへのパスで初期化するため、outlook は他の状態で変更を認識できるようになります。</span><span class="sxs-lookup"><span data-stu-id="92611-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="92611-122">クライアントは、**同期**の [in] メンバーを設定します。これは、Outlook に他の状態を処理する方法を指示します。</span><span class="sxs-lookup"><span data-stu-id="92611-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="92611-123">たとえば、クライアントは*ulflags*を**UPS_UPLOAD_ONLY**および**UPS_THESE_FOLDERS**および*pel*に設定して、フォルダーのエントリ識別子のリストを、これらのフォルダーのみがアップロードされることを Outlook に通知することができます。</span><span class="sxs-lookup"><span data-stu-id="92611-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="92611-124">この状態が終了すると、ローカルストアはアイドル状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="92611-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92611-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="92611-125">See also</span></span>



[<span data-ttu-id="92611-126">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="92611-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="92611-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="92611-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="92611-128">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="92611-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="92611-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="92611-129">SYNCSTATE</span></span>](syncstate.md)

