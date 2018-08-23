---
title: 同期状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d9f2a11a9ec1691863b476fed02eff1831a69207
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569723"
---
# <a name="synchronize-state"></a><span data-ttu-id="8cb36-103">同期状態</span><span class="sxs-lookup"><span data-stu-id="8cb36-103">Synchronize State</span></span>

  
  
<span data-ttu-id="8cb36-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cb36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8cb36-105">このトピックでは、レプリケーションの状態マシンの同期状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="8cb36-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8cb36-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="8cb36-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8cb36-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="8cb36-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="8cb36-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="8cb36-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="8cb36-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="8cb36-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="8cb36-110">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="8cb36-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="8cb36-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="8cb36-111">From this state:</span></span>  <br/> |[<span data-ttu-id="8cb36-112">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="8cb36-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="8cb36-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="8cb36-113">To this state:</span></span>  <br/> |<span data-ttu-id="8cb36-114">[階層の状態をダウンロード](download-hierarchy-state.md)[内容の状態を同期](synchronize-contents-state.md)[階層の状態をアップロード](upload-hierarchy-state.md)、またはアイドル状態</span><span class="sxs-lookup"><span data-stu-id="8cb36-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8cb36-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="8cb36-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="8cb36-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8cb36-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="8cb36-117">説明</span><span class="sxs-lookup"><span data-stu-id="8cb36-117">Description</span></span>

<span data-ttu-id="8cb36-118">この状態では、同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="8cb36-118">This state initiates synchronization.</span></span> <span data-ttu-id="8cb36-119">ローカル ストアは、ここからアップロードまたはダウンロードの状態に移行できます。</span><span class="sxs-lookup"><span data-stu-id="8cb36-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="8cb36-120">ローカル ストアは、フォルダー階層をサーバーにアップロードするアップロード階層状態に移行できるなど、階層を最初にアップロードしてからダウンロードして階層、サーバーから完全な同期を実行できます。</span><span class="sxs-lookup"><span data-stu-id="8cb36-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="8cb36-121">この状態の時に Outlook は、Outlook がその他の状態の時に変更を表示するようにローカル ストアへのパスに関連付けられている**同期**データ構造体を初期化します。</span><span class="sxs-lookup"><span data-stu-id="8cb36-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="8cb36-122">クライアントが、[in] 設定の**同期**Outlook の他の状態を処理する方法を指示するメンバーです。</span><span class="sxs-lookup"><span data-stu-id="8cb36-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="8cb36-123">たとえば、クライアントは**UPS_UPLOAD_ONLY**と**UPS_THESE_FOLDERS**に*ulFlags*を設定することができ、アップロードされるとこれらのフォルダーのみを Outlook に指示するのにはフォルダーのエントリ id の一覧には、 *pel* 。</span><span class="sxs-lookup"><span data-stu-id="8cb36-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="8cb36-124">この状態が終了すると、ローカル ストアは、アイドル状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="8cb36-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8cb36-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="8cb36-125">See also</span></span>



[<span data-ttu-id="8cb36-126">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="8cb36-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="8cb36-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="8cb36-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8cb36-128">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="8cb36-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8cb36-129">同期状態</span><span class="sxs-lookup"><span data-stu-id="8cb36-129">SYNCSTATE</span></span>](syncstate.md)

