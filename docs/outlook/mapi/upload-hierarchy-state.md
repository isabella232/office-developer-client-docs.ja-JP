---
title: 階層アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d53790cb51b660c781190cf41ca317c823a021e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804186"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="1d9cd-103">階層アップロード状態</span><span class="sxs-lookup"><span data-stu-id="1d9cd-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="1d9cd-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d9cd-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="1d9cd-105">このトピックでは、レプリケーション状態マシンのアップロードの階層状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1d9cd-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1d9cd-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d9cd-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="1d9cd-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="1d9cd-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="1d9cd-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="1d9cd-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-111">From this state:</span></span>  <br/> |[<span data-ttu-id="1d9cd-112">状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="1d9cd-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-113">To this state:</span></span>  <br/> |<span data-ttu-id="1d9cd-114">[フォルダーの状態をアップロード](upload-folder-state.md)するか、または状態の同期</span><span class="sxs-lookup"><span data-stu-id="1d9cd-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="1d9cd-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="1d9cd-116">クライアントを別の状態が 1 つの出発は、後者から以前に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="1d9cd-117">説明</span><span class="sxs-lookup"><span data-stu-id="1d9cd-117">Description</span></span>

<span data-ttu-id="1d9cd-118">この状態状態を同期する開始の直前に指定されているフォルダー ツリーの階層にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="1d9cd-119">Outlook では、作成またはその階層および初期化*セント* **UPHIER**内で変更されたフォルダーの数を決定します。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="1d9cd-120">Outlook では、他のメンバー *iEnt*にアップロードしたフォルダーの数のカウントも維持されます。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="1d9cd-121">*セント*のフォルダーをアップロードするには、クライアントは、フォルダーのアップロードが終了したときに、アップロードの階層状態に戻すフォルダーのアップロードの状態にローカル ストアを移動します。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="1d9cd-122">アップロード階層の状態が終了するとローカル ストアを同期の状態を返します。</span><span class="sxs-lookup"><span data-stu-id="1d9cd-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d9cd-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d9cd-123">See also</span></span>



[<span data-ttu-id="1d9cd-124">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="1d9cd-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="1d9cd-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="1d9cd-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="1d9cd-126">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="1d9cd-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="1d9cd-127">同期状態</span><span class="sxs-lookup"><span data-stu-id="1d9cd-127">SYNCSTATE</span></span>](syncstate.md)

