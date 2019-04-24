---
title: 階層のアップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286316"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="8f416-103">階層のアップロード状態</span><span class="sxs-lookup"><span data-stu-id="8f416-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="8f416-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f416-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8f416-105">このトピックでは、レプリケーション状態マシンのアップロード階層の状態中に行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f416-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8f416-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="8f416-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f416-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="8f416-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="8f416-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="8f416-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="8f416-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="8f416-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="8f416-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="8f416-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="8f416-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="8f416-111">From this state:</span></span>  <br/> |[<span data-ttu-id="8f416-112">同期状態</span><span class="sxs-lookup"><span data-stu-id="8f416-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="8f416-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="8f416-113">To this state:</span></span>  <br/> |<span data-ttu-id="8f416-114">[フォルダーの状態のアップロード](upload-folder-state.md)、または同期の状態</span><span class="sxs-lookup"><span data-stu-id="8f416-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8f416-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="8f416-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="8f416-116">ある状態から別の状態にクライアントを出発するには、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f416-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="8f416-117">説明</span><span class="sxs-lookup"><span data-stu-id="8f416-117">Description</span></span>

<span data-ttu-id="8f416-118">この状態は、前の同期状態で指定されたフォルダーツリー階層のアップロードを開始します。</span><span class="sxs-lookup"><span data-stu-id="8f416-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="8f416-119">Outlook は、その階層で作成または変更されたフォルダーの数を\*\* 決定し、 **uphier**でを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8f416-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="8f416-120">また、Outlook では、別のメンバーのアップロードされた\*\* フォルダーの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f416-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="8f416-121">各*セント*folders をアップロードするために、クライアントはローカルストアを upload フォルダーの状態に移行し、フォルダーのアップロードが完了すると、アップロード階層の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="8f416-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="8f416-122">階層のアップロード状態が終了すると、ローカルストアは同期状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="8f416-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8f416-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="8f416-123">See also</span></span>



[<span data-ttu-id="8f416-124">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="8f416-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="8f416-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="8f416-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8f416-126">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="8f416-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8f416-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="8f416-127">SYNCSTATE</span></span>](syncstate.md)

