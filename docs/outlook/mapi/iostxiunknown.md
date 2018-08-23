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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7419a0df7a2f3b76caeeb1ca564624d437eddd52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801112"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="a759d-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a759d-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="a759d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a759d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a759d-105">同期メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="a759d-105">Provides synchronization methods.</span></span> <span data-ttu-id="a759d-106">このインターフェイスは、サーバーとローカル ストアに変更をサーバーにローカルでの変更をレプリケートするために必要な情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="a759d-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a759d-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="a759d-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="a759d-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="a759d-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="a759d-109">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="a759d-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a759d-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="a759d-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a759d-111">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="a759d-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a759d-112">発生しました</span><span class="sxs-lookup"><span data-stu-id="a759d-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="a759d-113">最後のエラーに関する情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="a759d-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="a759d-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="a759d-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="a759d-115">同期を開始しようとしていますが、ローカル ストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="a759d-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="a759d-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="a759d-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="a759d-117">特定の状態の同期をローカル ストアを準備し、複製に必要な情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="a759d-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="a759d-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="a759d-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="a759d-119">現在の状態で同期を終了し、その状態を終了します。</span><span class="sxs-lookup"><span data-stu-id="a759d-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="a759d-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="a759d-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="a759d-121">メッセージ ヘッダーの同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="a759d-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="a759d-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="a759d-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="a759d-123">メッセージ ヘッダーの同期を終了します。</span><span class="sxs-lookup"><span data-stu-id="a759d-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="a759d-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="a759d-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="a759d-125">同期の結果を設定します。</span><span class="sxs-lookup"><span data-stu-id="a759d-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="a759d-126">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="a759d-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a759d-127">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="a759d-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a759d-128">注釈</span><span class="sxs-lookup"><span data-stu-id="a759d-128">Remarks</span></span>

<span data-ttu-id="a759d-129">クライアントは、アップロードまたはフォルダーとローカル ストア上のフォルダーの内容を同期化、ローカル ストア 1 つの状態からに移動別で[レプリケーションの状態マシン](about-the-replication-state-machine.md)の状態遷移図で示されています。</span><span class="sxs-lookup"><span data-stu-id="a759d-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="a759d-130">ローカル ストアを別の 1 つの状態に移動するクライアントのイベントの順序は、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="a759d-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="a759d-131">クライアントでは、レプリケーションを開始しようとしていますが、ローカル ストアに通知するために**IOSTX::InitSync**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a759d-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="a759d-132">、複製し、複製するオブジェクトの方向によっては、クライアントは、適切な状態のレプリケーションを開始するのには**IOSTX::SyncBeg**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a759d-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="a759d-133">Outlook は、必要な情報をクライアントに提供し、クライアントがレプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="a759d-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="a759d-134">クライアントは、複製の結果を得るために**IOSTX::SetSyncResult**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a759d-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="a759d-135">クライアントは、Outlook の以降のレプリケーションに必要な情報を提供する、レプリケーションを終了するのには**IOSTX::SyncEnd**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a759d-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="a759d-136">具体的には、メッセージ アイテムをダウンロードするとき、クライアントを使用して、 **IOSTX::SyncHdrBeg**と**IOSTX::SyncHdrEnd**ローカル ストア内のメッセージ ヘッダーを持つすべてのメッセージ アイテムを更新します。</span><span class="sxs-lookup"><span data-stu-id="a759d-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="a759d-137">**IOSTX::SyncHdrBeg**、時に、ローカルは、メッセージ ヘッダーのダウンロードの状態に遷移を保存します。</span><span class="sxs-lookup"><span data-stu-id="a759d-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="a759d-138">最初に、outlook は、ローカル ストア内の現在のメッセージのヘッダーを使用して、クライアントを提供します。</span><span class="sxs-lookup"><span data-stu-id="a759d-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="a759d-139">クライアントは、メッセージ ヘッダーとメッセージの項目をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a759d-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="a759d-140">Outlook では、完全なメッセージ項目にローカル ストア上の項目を更新します。</span><span class="sxs-lookup"><span data-stu-id="a759d-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a759d-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="a759d-141">See also</span></span>



[<span data-ttu-id="a759d-142">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a759d-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a759d-143">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="a759d-143">MAPI Constants</span></span>](mapi-constants.md)

