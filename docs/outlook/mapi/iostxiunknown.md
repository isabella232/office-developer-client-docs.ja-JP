---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431996"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="e639d-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e639d-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="e639d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e639d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e639d-105">同期メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="e639d-105">Provides synchronization methods.</span></span> <span data-ttu-id="e639d-106">このインターフェイスは、サーバーとサーバーの変更をローカル ストアにレプリケートするために必要な情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="e639d-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e639d-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="e639d-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="e639d-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="e639d-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="e639d-109">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="e639d-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e639d-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="e639d-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e639d-111">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e639d-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e639d-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e639d-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="e639d-113">最後のエラーに関する拡張情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="e639d-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="e639d-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="e639d-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="e639d-115">同期が始まるとローカル ストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="e639d-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="e639d-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="e639d-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="e639d-117">特定の状態での同期のためにローカル ストアを準備し、レプリケートに必要な情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="e639d-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="e639d-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="e639d-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="e639d-119">現在の状態で同期を終了し、その状態を終了します。</span><span class="sxs-lookup"><span data-stu-id="e639d-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="e639d-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="e639d-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="e639d-121">メッセージ ヘッダーの同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="e639d-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="e639d-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="e639d-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="e639d-123">メッセージ ヘッダーの同期を終了します。</span><span class="sxs-lookup"><span data-stu-id="e639d-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="e639d-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="e639d-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="e639d-125">同期の結果を設定します。</span><span class="sxs-lookup"><span data-stu-id="e639d-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="e639d-126">*プレースホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e639d-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e639d-127">*サポートされていないか、文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="e639d-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e639d-128">注釈</span><span class="sxs-lookup"><span data-stu-id="e639d-128">Remarks</span></span>

<span data-ttu-id="e639d-129">クライアントは、ローカル ストア上のフォルダーとフォルダーの内容をアップロードまたは同期するときに、レプリケーションステート マシンについての状態遷移図に示されている状態から別の状態にローカル ストアを [移動します](about-the-replication-state-machine.md)。</span><span class="sxs-lookup"><span data-stu-id="e639d-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="e639d-130">クライアントがローカル ストアをある状態から別の状態に移動するイベントの順序を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e639d-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="e639d-131">クライアントは **IOSTX::InitSync** を呼び出して、レプリケーションが開始されるローカル ストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="e639d-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="e639d-132">レプリケーションの方向とレプリケートするオブジェクトに応じて、クライアントは **IOSTX::SyncBeg** を呼び出して、適切な状態でレプリケーションを開始します。</span><span class="sxs-lookup"><span data-stu-id="e639d-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="e639d-133">Outlook必要な情報をクライアントに提供し、クライアントがレプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="e639d-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="e639d-134">クライアントは **IOSTX::SetSyncResult** を呼び出して、レプリケーションの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="e639d-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="e639d-135">クライアントは **IOSTX::SyncEnd** を呼び出してレプリケーションを終了し、Outlookに必要な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e639d-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="e639d-136">特に、メッセージ アイテムをダウンロードする場合、クライアントは **IOSTX::SyncHdrBeg** と **IOSTX::SyncHdrEnd** を使用して、ローカル ストアのメッセージ ヘッダーを使用して完全なメッセージ アイテムを更新します。</span><span class="sxs-lookup"><span data-stu-id="e639d-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="e639d-137">**IOSTX::SyncHdrBeg** の場合、ローカル ストアはダウンロード メッセージ ヘッダーの状態に移行します。</span><span class="sxs-lookup"><span data-stu-id="e639d-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="e639d-138">Outlook、クライアントにローカル ストアの現在のメッセージ ヘッダーを提供します。</span><span class="sxs-lookup"><span data-stu-id="e639d-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="e639d-139">クライアントは、メッセージ ヘッダーと共に完全なメッセージ アイテムをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e639d-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="e639d-140">Outlook完全なメッセージ アイテムを使用してローカル ストアのアイテムを更新します。</span><span class="sxs-lookup"><span data-stu-id="e639d-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e639d-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="e639d-141">See also</span></span>



[<span data-ttu-id="e639d-142">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="e639d-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e639d-143">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="e639d-143">MAPI Constants</span></span>](mapi-constants.md)

