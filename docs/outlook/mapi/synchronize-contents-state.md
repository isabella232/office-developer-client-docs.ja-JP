---
title: コンテンツ同期状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a2bdbeb39cce1e62569f364875c3828cdd530c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577248"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="aedbc-103">コンテンツ同期状態</span><span class="sxs-lookup"><span data-stu-id="aedbc-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="aedbc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aedbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="aedbc-105">このトピックでは、同期内容マシンの状態、レプリケーション状態中の動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="aedbc-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="aedbc-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="aedbc-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aedbc-107">状態識別子。</span><span class="sxs-lookup"><span data-stu-id="aedbc-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="aedbc-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="aedbc-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="aedbc-109">関連するデータ構造体。</span><span class="sxs-lookup"><span data-stu-id="aedbc-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="aedbc-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="aedbc-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="aedbc-111">この状態。</span><span class="sxs-lookup"><span data-stu-id="aedbc-111">From this state:</span></span>  <br/> |[<span data-ttu-id="aedbc-112">状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="aedbc-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="aedbc-113">この状態。</span><span class="sxs-lookup"><span data-stu-id="aedbc-113">To this state:</span></span>  <br/> |<span data-ttu-id="aedbc-114">[テーブルの状態をダウンロード](download-table-state.md)[テーブルの状態をアップロード](upload-table-state.md)、または状態の同期</span><span class="sxs-lookup"><span data-stu-id="aedbc-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="aedbc-115">レプリケーションの状態マシンは、確定的なステート マシンです。</span><span class="sxs-lookup"><span data-stu-id="aedbc-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="aedbc-116">クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="aedbc-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="aedbc-117">説明</span><span class="sxs-lookup"><span data-stu-id="aedbc-117">Description</span></span>

<span data-ttu-id="aedbc-118">この状態が 2 つのレプリケーション ・ プロセスのいずれかを開始する: ローカル ストアでは、または完全に同期フォルダーを指定の内容をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="aedbc-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="aedbc-119">指定のフォルダーの完全な同期で、内容が先にアップロードし、ダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="aedbc-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="aedbc-120">状態の同期によっては、上記の「対応する**[同期](sync.md)** 構造体に設定された*ulFlags* Outlook が [出力] コンテンツに関する情報を提供する**SYNCCONT**構造体のメンバー初期化します。</span><span class="sxs-lookup"><span data-stu-id="aedbc-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="aedbc-121">同じの**SYNCCONT**構造体を使って、クライアントをアップロードまたはダウンロードするコンテンツを持つフォルダーの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="aedbc-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="aedbc-122">クライアントは、フォルダーをアップロードするアップロードの表の状態にローカル ストアを移動またはフォルダーをダウンロードするダウンロードのテーブルの状態をローカル ストアに移動して、これらのフォルダーをループします。</span><span class="sxs-lookup"><span data-stu-id="aedbc-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="aedbc-123">さらに、クライアントでは、レプリケーションを必要とするフォルダーのエントリ Id を取得します。</span><span class="sxs-lookup"><span data-stu-id="aedbc-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="aedbc-124">この状態が終了すると、Outlook は、その内部の情報をクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="aedbc-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="aedbc-125">ローカル ストアは、同期の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="aedbc-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aedbc-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="aedbc-126">See also</span></span>



[<span data-ttu-id="aedbc-127">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="aedbc-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="aedbc-128">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="aedbc-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="aedbc-129">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="aedbc-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="aedbc-130">同期状態</span><span class="sxs-lookup"><span data-stu-id="aedbc-130">SYNCSTATE</span></span>](syncstate.md)

