---
title: 状態の同期
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414628"
---
# <a name="synchronize-state"></a><span data-ttu-id="a405b-103">状態の同期</span><span class="sxs-lookup"><span data-stu-id="a405b-103">Synchronize State</span></span>

  
  
<span data-ttu-id="a405b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a405b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a405b-105">このトピックでは、レプリケーションステート マシンの同期状態の間に何が起こるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="a405b-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a405b-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a405b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a405b-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="a405b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a405b-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="a405b-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="a405b-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="a405b-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="a405b-110">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="a405b-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="a405b-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="a405b-111">From this state:</span></span>  <br/> |[<span data-ttu-id="a405b-112">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="a405b-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="a405b-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="a405b-113">To this state:</span></span>  <br/> |<span data-ttu-id="a405b-114">[階層状態のダウンロード](download-hierarchy-state.md)、[コンテンツの状態の同期、](synchronize-contents-state.md)[階層のアップロード状態](upload-hierarchy-state.md)、またはアイドル状態</span><span class="sxs-lookup"><span data-stu-id="a405b-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a405b-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="a405b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a405b-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="a405b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a405b-117">説明</span><span class="sxs-lookup"><span data-stu-id="a405b-117">Description</span></span>

<span data-ttu-id="a405b-118">この状態では、同期が開始されます。</span><span class="sxs-lookup"><span data-stu-id="a405b-118">This state initiates synchronization.</span></span> <span data-ttu-id="a405b-119">ローカル ストアは、ここからアップロードまたはダウンロード状態に移行できます。</span><span class="sxs-lookup"><span data-stu-id="a405b-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="a405b-120">たとえば、ローカル ストアをアップロード階層状態に移動してフォルダー階層をサーバーにアップロードしたり、最初に階層をアップロードしてからサーバーから階層をダウンロードすることで、完全な同期を実行できます。</span><span class="sxs-lookup"><span data-stu-id="a405b-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="a405b-121">この状態の間Outlook、ローカル ストアへのパスを使用して関連付けられた **SYNC** データ構造を初期化し、Outlook状態の間に変更が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a405b-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="a405b-122">クライアントは SYNC の [in] メンバーを設定し、他Outlookを処理する方法を示します。 </span><span class="sxs-lookup"><span data-stu-id="a405b-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="a405b-123">たとえば、クライアントは **、ulFlags** を UPS_UPLOAD_ONLY および **UPS_THESE_FOLDERS** に設定し、フォルダーのエントリ識別子の一覧に pel を設定して、Outlook にこれらのフォルダーだけがアップロードされるというメッセージを表示できます。</span><span class="sxs-lookup"><span data-stu-id="a405b-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="a405b-124">この状態が終了すると、ローカル ストアはアイドル状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="a405b-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a405b-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a405b-125">See also</span></span>



[<span data-ttu-id="a405b-126">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a405b-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a405b-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="a405b-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a405b-128">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="a405b-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a405b-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a405b-129">SYNCSTATE</span></span>](syncstate.md)

