---
title: 読み取り状態のアップロードの状態
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
# <a name="upload-read-status-state"></a><span data-ttu-id="b1b1a-103">読み取り状態のアップロードの状態</span><span class="sxs-lookup"><span data-stu-id="b1b1a-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="b1b1a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1b1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b1b1a-105">このトピックでは、レプリケーション状態マシンの読み取り状態のアップロード中に行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1b1a-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b1b1a-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b1b1a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1b1a-107">状態識別子:</span><span class="sxs-lookup"><span data-stu-id="b1b1a-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b1b1a-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="b1b1a-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="b1b1a-109">関連データ構造:</span><span class="sxs-lookup"><span data-stu-id="b1b1a-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b1b1a-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="b1b1a-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="b1b1a-111">この状態から:</span><span class="sxs-lookup"><span data-stu-id="b1b1a-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b1b1a-112">テーブルの状態をアップロードする</span><span class="sxs-lookup"><span data-stu-id="b1b1a-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="b1b1a-113">この状態:</span><span class="sxs-lookup"><span data-stu-id="b1b1a-113">To this state:</span></span>  <br/> |<span data-ttu-id="b1b1a-114">テーブルの状態をアップロードする</span><span class="sxs-lookup"><span data-stu-id="b1b1a-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b1b1a-115">レプリケーション状態マシンは、確定状態のマシンです。</span><span class="sxs-lookup"><span data-stu-id="b1b1a-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b1b1a-116">ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1b1a-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b1b1a-117">説明</span><span class="sxs-lookup"><span data-stu-id="b1b1a-117">Description</span></span>

<span data-ttu-id="b1b1a-118">この状態は、前のアップロードテーブル状態で指定されたフォルダー内のアイテムの読み取り状態のアップロードを開始します。</span><span class="sxs-lookup"><span data-stu-id="b1b1a-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="b1b1a-119">この状態の間、Outlook は、関連付けられた**upread**データ構造と、読み取り状態が変更されたフォルダー内のアイテムに関する情報を初期化します。</span><span class="sxs-lookup"><span data-stu-id="b1b1a-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="b1b1a-120">クライアントは、サーバー上のこれらのアイテムの読み取り状態を、読み取りまたは未読に更新します。</span><span class="sxs-lookup"><span data-stu-id="b1b1a-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="b1b1a-121">この状態が終了すると、Outlook はアイテムの読み取り状態に関する内部情報をクリアし、アイテムの開封状態が再度アップロードされるのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="b1b1a-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="b1b1a-122">ローカルストアは、テーブルのアップロード状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="b1b1a-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1b1a-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1b1a-123">See also</span></span>



[<span data-ttu-id="b1b1a-124">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="b1b1a-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b1b1a-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="b1b1a-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b1b1a-126">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="b1b1a-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b1b1a-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="b1b1a-127">SYNCSTATE</span></span>](syncstate.md)

