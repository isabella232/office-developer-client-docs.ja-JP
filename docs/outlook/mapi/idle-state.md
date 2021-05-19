---
title: アイドル状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419479"
---
# <a name="idle-state"></a><span data-ttu-id="0f690-103">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="0f690-103">Idle State</span></span>

  
  
<span data-ttu-id="0f690-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f690-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="0f690-105">このトピックでは、レプリケーションステート マシンのアイドル状態の間に何が起こるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="0f690-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0f690-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="0f690-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f690-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="0f690-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="0f690-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="0f690-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="0f690-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="0f690-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="0f690-110">*なし*</span><span class="sxs-lookup"><span data-stu-id="0f690-110">*None*</span></span>  <br/> |
|<span data-ttu-id="0f690-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="0f690-111">From this state:</span></span>  <br/> | <span data-ttu-id="0f690-112">*該当なし*</span><span class="sxs-lookup"><span data-stu-id="0f690-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="0f690-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="0f690-113">To this state:</span></span>  <br/> |[<span data-ttu-id="0f690-114">同期状態</span><span class="sxs-lookup"><span data-stu-id="0f690-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="0f690-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="0f690-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="0f690-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f690-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="0f690-117">説明</span><span class="sxs-lookup"><span data-stu-id="0f690-117">Description</span></span>

<span data-ttu-id="0f690-118">この状態では何も起こりません。</span><span class="sxs-lookup"><span data-stu-id="0f690-118">Nothing happens in this state.</span></span> <span data-ttu-id="0f690-119">ローカル ストアは、レプリケーションが開始される前とレプリケーションが完了した後に、この状態になります。</span><span class="sxs-lookup"><span data-stu-id="0f690-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0f690-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f690-120">See also</span></span>



[<span data-ttu-id="0f690-121">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="0f690-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="0f690-122">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="0f690-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="0f690-123">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="0f690-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="0f690-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="0f690-124">SYNCSTATE</span></span>](syncstate.md)

