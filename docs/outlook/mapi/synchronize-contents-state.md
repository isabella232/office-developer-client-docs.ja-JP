---
title: コンテンツの状態の同期
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438471"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="86fb2-103">コンテンツの状態の同期</span><span class="sxs-lookup"><span data-stu-id="86fb2-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="86fb2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86fb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="86fb2-105">このトピックでは、レプリケーション状態マシンのコンテンツ同期状態中の処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="86fb2-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="86fb2-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="86fb2-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86fb2-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="86fb2-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="86fb2-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="86fb2-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="86fb2-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="86fb2-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="86fb2-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="86fb2-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="86fb2-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="86fb2-111">From this state:</span></span>  <br/> |[<span data-ttu-id="86fb2-112">同期状態</span><span class="sxs-lookup"><span data-stu-id="86fb2-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="86fb2-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="86fb2-113">To this state:</span></span>  <br/> |<span data-ttu-id="86fb2-114">[テーブルの状態のダウンロード](download-table-state.md)、[テーブルの状態のアップロード](upload-table-state.md)、または同期の状態</span><span class="sxs-lookup"><span data-stu-id="86fb2-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="86fb2-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="86fb2-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="86fb2-116">ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="86fb2-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="86fb2-117">説明</span><span class="sxs-lookup"><span data-stu-id="86fb2-117">Description</span></span>

<span data-ttu-id="86fb2-118">この状態は、次の2つのレプリケーションプロセスのうちの1つを開始します。ローカルストアの指定したフォルダーの内容をアップロードするか、完全な同期を行います。</span><span class="sxs-lookup"><span data-stu-id="86fb2-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="86fb2-119">完全同期では、指定された各フォルダーについて、コンテンツが最初にアップロードされてからダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="86fb2-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="86fb2-120">前の同期状態で対応する**[同期](sync.md)** 構造で設定されている*ulflags*に応じて、Outlook はコンテンツに関する情報を提供するために**synccont**構造で [out] メンバーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="86fb2-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="86fb2-121">同じ synccont \*\*\*\* 構造を使用して、クライアントはコンテンツをアップロードまたはダウンロードするフォルダーの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="86fb2-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="86fb2-122">クライアントは、ローカルストアをアップロードテーブルの状態に移動してフォルダーをアップロードするか、ローカルストアをダウンロードテーブルの状態に移動してフォルダーをダウンロードすることで、これらの各フォルダーをループ処理します。</span><span class="sxs-lookup"><span data-stu-id="86fb2-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="86fb2-123">さらに、クライアントはレプリケーションを必要とするフォルダーのエントリ id を取得します。</span><span class="sxs-lookup"><span data-stu-id="86fb2-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="86fb2-124">この状態が終了すると、Outlook は内部情報をクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="86fb2-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="86fb2-125">ローカルストアが同期状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="86fb2-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86fb2-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="86fb2-126">See also</span></span>



[<span data-ttu-id="86fb2-127">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="86fb2-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="86fb2-128">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="86fb2-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="86fb2-129">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="86fb2-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="86fb2-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="86fb2-130">SYNCSTATE</span></span>](syncstate.md)

