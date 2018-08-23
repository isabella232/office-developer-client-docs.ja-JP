---
title: アイドル状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dbe81a2a27f302a38eba6f3c5045df905d8db682
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800417"
---
# <a name="idle-state"></a><span data-ttu-id="abf26-103">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="abf26-103">Idle State</span></span>

  
  
<span data-ttu-id="abf26-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="abf26-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="abf26-105">このトピックでは、レプリケーションの状態のコンピューターのアイドル状態のときに動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="abf26-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="abf26-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="abf26-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abf26-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="abf26-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="abf26-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="abf26-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="abf26-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="abf26-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="abf26-110">*None*</span><span class="sxs-lookup"><span data-stu-id="abf26-110">*None*</span></span>  <br/> |
|<span data-ttu-id="abf26-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="abf26-111">From this state:</span></span>  <br/> | <span data-ttu-id="abf26-112">*該当なし*</span><span class="sxs-lookup"><span data-stu-id="abf26-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="abf26-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="abf26-113">To this state:</span></span>  <br/> |[<span data-ttu-id="abf26-114">状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="abf26-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="abf26-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="abf26-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="abf26-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="abf26-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="abf26-117">説明</span><span class="sxs-lookup"><span data-stu-id="abf26-117">Description</span></span>

<span data-ttu-id="abf26-118">この状態で何も起こりません。</span><span class="sxs-lookup"><span data-stu-id="abf26-118">Nothing happens in this state.</span></span> <span data-ttu-id="abf26-119">ローカル ストアは、レプリケーションが完了した後、レプリケーションを開始する前にこの状態では。</span><span class="sxs-lookup"><span data-stu-id="abf26-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="abf26-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="abf26-120">See also</span></span>



[<span data-ttu-id="abf26-121">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="abf26-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="abf26-122">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="abf26-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="abf26-123">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="abf26-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="abf26-124">同期状態</span><span class="sxs-lookup"><span data-stu-id="abf26-124">SYNCSTATE</span></span>](syncstate.md)

