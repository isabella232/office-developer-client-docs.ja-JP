---
title: アップロード状態の読み取り
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431541"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="a9ef8-103">アップロード状態の読み取り</span><span class="sxs-lookup"><span data-stu-id="a9ef8-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="a9ef8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9ef8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a9ef8-105">このトピックでは、レプリケーションステート マシンのアップロード読み取り状態状態の間に発生する処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="a9ef8-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a9ef8-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a9ef8-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9ef8-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="a9ef8-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a9ef8-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="a9ef8-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="a9ef8-109">関連するデータ構造:</span><span class="sxs-lookup"><span data-stu-id="a9ef8-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="a9ef8-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="a9ef8-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="a9ef8-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="a9ef8-111">From this state:</span></span>  <br/> |[<span data-ttu-id="a9ef8-112">アップロード状態</span><span class="sxs-lookup"><span data-stu-id="a9ef8-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="a9ef8-113">この状態に:</span><span class="sxs-lookup"><span data-stu-id="a9ef8-113">To this state:</span></span>  <br/> |<span data-ttu-id="a9ef8-114">アップロード状態</span><span class="sxs-lookup"><span data-stu-id="a9ef8-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a9ef8-115">レプリケーションステート マシンは、デターミニスティックステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="a9ef8-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a9ef8-116">ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9ef8-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a9ef8-117">説明</span><span class="sxs-lookup"><span data-stu-id="a9ef8-117">Description</span></span>

<span data-ttu-id="a9ef8-118">この状態では、前のアップロード テーブルの状態で指定されたフォルダー内のアイテムの読み取り状態のアップロードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="a9ef8-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="a9ef8-119">この状態の間Outlook、読み取り状態が変更されたフォルダー内のアイテムに関する情報を使用して、関連付けられた **UPREAD** データ構造を初期化します。</span><span class="sxs-lookup"><span data-stu-id="a9ef8-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="a9ef8-120">クライアントは、サーバー上のこれらのアイテムの読み取り状態を読み取りまたは未読として更新します。</span><span class="sxs-lookup"><span data-stu-id="a9ef8-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="a9ef8-121">この状態が終了するとOutlookアイテムの読み取り状態に関する内部情報が消去され、アイテムの読み取り状態が再びアップロードされなくります。</span><span class="sxs-lookup"><span data-stu-id="a9ef8-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="a9ef8-122">ローカル ストアは、アップロード テーブルの状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="a9ef8-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9ef8-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9ef8-123">See also</span></span>



[<span data-ttu-id="a9ef8-124">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a9ef8-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a9ef8-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="a9ef8-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a9ef8-126">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="a9ef8-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a9ef8-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a9ef8-127">SYNCSTATE</span></span>](syncstate.md)

