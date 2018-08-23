---
title: アイドル状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b74ecb44d9a38fc73ceed4077d6f7a939f92f5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591801"
---
# <a name="idle-state"></a><span data-ttu-id="2c2f6-103">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="2c2f6-103">Idle State</span></span>

  
  
<span data-ttu-id="2c2f6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c2f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2c2f6-105">このトピックでは、レプリケーションの状態のコンピューターのアイドル状態のときに動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2c2f6-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2c2f6-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c2f6-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="2c2f6-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="2c2f6-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="2c2f6-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="2c2f6-110">*None*</span><span class="sxs-lookup"><span data-stu-id="2c2f6-110">*None*</span></span>  <br/> |
|<span data-ttu-id="2c2f6-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-111">From this state:</span></span>  <br/> | <span data-ttu-id="2c2f6-112">*該当なし*</span><span class="sxs-lookup"><span data-stu-id="2c2f6-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="2c2f6-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-113">To this state:</span></span>  <br/> |[<span data-ttu-id="2c2f6-114">状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="2c2f6-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="2c2f6-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="2c2f6-117">説明</span><span class="sxs-lookup"><span data-stu-id="2c2f6-117">Description</span></span>

<span data-ttu-id="2c2f6-118">この状態で何も起こりません。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-118">Nothing happens in this state.</span></span> <span data-ttu-id="2c2f6-119">ローカル ストアは、レプリケーションが完了した後、レプリケーションを開始する前にこの状態では。</span><span class="sxs-lookup"><span data-stu-id="2c2f6-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c2f6-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c2f6-120">See also</span></span>



[<span data-ttu-id="2c2f6-121">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="2c2f6-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2c2f6-122">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="2c2f6-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2c2f6-123">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="2c2f6-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2c2f6-124">同期状態</span><span class="sxs-lookup"><span data-stu-id="2c2f6-124">SYNCSTATE</span></span>](syncstate.md)

