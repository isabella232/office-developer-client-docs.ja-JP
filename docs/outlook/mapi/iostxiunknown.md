---
title: iostx IUnknown
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
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317179"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="20baf-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20baf-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="20baf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20baf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20baf-105">同期方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="20baf-105">Provides synchronization methods.</span></span> <span data-ttu-id="20baf-106">このインターフェイスでは、ローカルの変更をサーバーにレプリケートするために必要な情報と、ローカルストアに対するサーバーの変更を取得します。</span><span class="sxs-lookup"><span data-stu-id="20baf-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20baf-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="20baf-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="20baf-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="20baf-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="20baf-109">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="20baf-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="20baf-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="20baf-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="20baf-111">v の順序</span><span class="sxs-lookup"><span data-stu-id="20baf-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="20baf-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="20baf-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="20baf-113">最新のエラーに関する拡張情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="20baf-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="20baf-114">initsync</span><span class="sxs-lookup"><span data-stu-id="20baf-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="20baf-115">同期が開始されることをローカルストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="20baf-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="20baf-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="20baf-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="20baf-117">特定の状態の同期用にローカルストアを準備し、レプリケートするために必要な情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="20baf-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="20baf-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="20baf-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="20baf-119">現在の状態で同期を終了し、その状態を終了します。</span><span class="sxs-lookup"><span data-stu-id="20baf-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="20baf-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="20baf-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="20baf-121">メッセージヘッダーの同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="20baf-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="20baf-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="20baf-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="20baf-123">メッセージヘッダーの同期を終了します。</span><span class="sxs-lookup"><span data-stu-id="20baf-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="20baf-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="20baf-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="20baf-125">同期の結果を設定します。</span><span class="sxs-lookup"><span data-stu-id="20baf-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="20baf-126">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="20baf-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="20baf-127">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="20baf-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20baf-128">解説</span><span class="sxs-lookup"><span data-stu-id="20baf-128">Remarks</span></span>

<span data-ttu-id="20baf-129">クライアントがローカルストアのフォルダーとフォルダーの内容をアップロードまたは同期すると、[レプリケーションステートマシンについて](about-the-replication-state-machine.md)の状態遷移図に示されているように、ローカルストアをある状態から別の状態に移動します。</span><span class="sxs-lookup"><span data-stu-id="20baf-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="20baf-130">クライアントがローカルストアをある状態から別の状態に移動する際のイベントの順序を次に示します。</span><span class="sxs-lookup"><span data-stu-id="20baf-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="20baf-131">クライアントは**iostx:: initsync**を呼び出して、レプリケーションが開始されようとしていることをローカルストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="20baf-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="20baf-132">レプリケーションの方向とレプリケートするオブジェクトに応じて、クライアントは**iostx:: SyncBeg**を呼び出して、適切な状態でレプリケーションを開始します。</span><span class="sxs-lookup"><span data-stu-id="20baf-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="20baf-133">Outlook はクライアントに必要な情報を提供し、クライアントはレプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="20baf-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="20baf-134">クライアントは**iostx:: SetSyncResult**を呼び出して、レプリケーションの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="20baf-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="20baf-135">クライアントは**iostx:: syncend**を呼び出してレプリケーションを終了し、次のレプリケーションに必要な情報を Outlook に提供します。</span><span class="sxs-lookup"><span data-stu-id="20baf-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="20baf-136">特に、メッセージアイテムをダウンロードする場合、クライアントは**iostx:: SyncHdrBeg**および**iostx:: SyncHdrEnd**を使用して、完全なメッセージアイテムをローカルストアのメッセージヘッダーで更新します。</span><span class="sxs-lookup"><span data-stu-id="20baf-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="20baf-137">**iostx:: SyncHdrBeg**では、ローカルストアはダウンロードメッセージヘッダーの状態に遷移します。</span><span class="sxs-lookup"><span data-stu-id="20baf-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="20baf-138">Outlook では、最初にクライアントに現在のメッセージヘッダーがローカルストアに提供されます。</span><span class="sxs-lookup"><span data-stu-id="20baf-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="20baf-139">クライアントは、メッセージヘッダーと共にメッセージアイテム全体をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="20baf-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="20baf-140">Outlook は、ローカルストア上のアイテムを完全なメッセージアイテムで更新します。</span><span class="sxs-lookup"><span data-stu-id="20baf-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20baf-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="20baf-141">See also</span></span>



[<span data-ttu-id="20baf-142">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="20baf-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="20baf-143">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="20baf-143">MAPI Constants</span></span>](mapi-constants.md)

