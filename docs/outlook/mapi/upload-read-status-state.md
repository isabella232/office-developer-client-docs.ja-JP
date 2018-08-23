---
title: 読み取り状況アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 172eaf47d305cf6e4d1ba54ceb4ac4b4feab80e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804183"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="29cac-103">読み取り状況アップロード状態</span><span class="sxs-lookup"><span data-stu-id="29cac-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="29cac-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29cac-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="29cac-105">このトピックでは、状態マシンの状態、レプリケーションの状態を読み取り、アップロード中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="29cac-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="29cac-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="29cac-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29cac-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="29cac-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="29cac-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="29cac-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="29cac-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="29cac-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="29cac-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="29cac-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="29cac-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="29cac-111">From this state:</span></span>  <br/> |[<span data-ttu-id="29cac-112">テーブルの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="29cac-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="29cac-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="29cac-113">To this state:</span></span>  <br/> |<span data-ttu-id="29cac-114">テーブルの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="29cac-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="29cac-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="29cac-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="29cac-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="29cac-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="29cac-117">説明</span><span class="sxs-lookup"><span data-stu-id="29cac-117">Description</span></span>

<span data-ttu-id="29cac-118">この状態は、上記アップロード テーブルの状態で指定したフォルダー内のアイテムの読み取り状態をアップロードを開始します。</span><span class="sxs-lookup"><span data-stu-id="29cac-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="29cac-119">この状態は、中には、Outlook は、リードのステータスが変更されたフォルダー内の項目の情報が関連付けられている**UPREAD**データ構造体を初期化します。</span><span class="sxs-lookup"><span data-stu-id="29cac-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="29cac-120">クライアントは、これらのアイテムを開封済みまたは未読にするとサーバー上の読み取り状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="29cac-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="29cac-121">この状態が終了すると Outlook は、もう一度アップロードしてから、アイテムの読み取り状態を防止するアイテムの読み取りの状態に関する内部情報を消去します。</span><span class="sxs-lookup"><span data-stu-id="29cac-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="29cac-122">ローカル ストアは、アップロード ・ テーブルの状態を返します。</span><span class="sxs-lookup"><span data-stu-id="29cac-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29cac-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="29cac-123">See also</span></span>



[<span data-ttu-id="29cac-124">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="29cac-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="29cac-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="29cac-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="29cac-126">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="29cac-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="29cac-127">同期状態</span><span class="sxs-lookup"><span data-stu-id="29cac-127">SYNCSTATE</span></span>](syncstate.md)

