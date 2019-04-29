---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411940"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="752f4-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="752f4-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="752f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="752f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="752f4-105">特定の状態の同期用にローカルストアを準備し、レプリケートするために必要な情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="752f4-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="752f4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="752f4-106">Parameters</span></span>

 <span data-ttu-id="752f4-107">_uisync_</span><span class="sxs-lookup"><span data-stu-id="752f4-107">_uiSync_</span></span>
  
>  <span data-ttu-id="752f4-108">順番ローカルストアが入力する状態。</span><span class="sxs-lookup"><span data-stu-id="752f4-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="752f4-109">state 識別子のリストを次に示します。</span><span class="sxs-lookup"><span data-stu-id="752f4-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="752f4-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="752f4-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="752f4-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="752f4-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="752f4-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="752f4-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="752f4-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="752f4-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="752f4-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="752f4-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="752f4-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="752f4-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="752f4-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="752f4-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="752f4-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="752f4-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="752f4-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="752f4-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="752f4-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="752f4-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="752f4-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="752f4-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="752f4-121">_ppv_</span><span class="sxs-lookup"><span data-stu-id="752f4-121">_ppv_</span></span>
  
>  <span data-ttu-id="752f4-122">[in]/[out] 入力する状態に対応するデータ構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="752f4-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="752f4-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="752f4-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="752f4-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="752f4-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="752f4-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="752f4-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="752f4-126">SYNC</span><span class="sxs-lookup"><span data-stu-id="752f4-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="752f4-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="752f4-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="752f4-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="752f4-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="752f4-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="752f4-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="752f4-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="752f4-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="752f4-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="752f4-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="752f4-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="752f4-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="752f4-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="752f4-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="752f4-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="752f4-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="752f4-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="752f4-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="752f4-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="752f4-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="752f4-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="752f4-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="752f4-138">注釈</span><span class="sxs-lookup"><span data-stu-id="752f4-138">Remarks</span></span>

<span data-ttu-id="752f4-139">クライアントは**[iostx:: SetSyncResult](iostx-setsyncresult.md)** を呼び出して、同期の結果を設定した後、 **[iostx:: syncend](iostx-syncend.md)** を呼び出してその状態を終了します。</span><span class="sxs-lookup"><span data-stu-id="752f4-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="752f4-140">クライアントは、状態が正常にレプリケートされたかどうかを判断するために、 **iostx** :: SyncBeg への各呼び出しに**[iostx:: syncend](iostx-syncend.md)** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="752f4-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="752f4-141">これが決定されると、Outlook は内部状態のクリーンアップを開始できるようになります。</span><span class="sxs-lookup"><span data-stu-id="752f4-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="752f4-142">これらの構造のほとんどには [out]/[in] 情報が含まれており、outlook が情報をクライアントに渡し、クライアントが outlook に情報を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="752f4-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="752f4-143">クライアントが**iostx:: SyncBeg**を呼び出すと、Outlook は指定された状態のデータ構造を割り当て、その状態の情報で初期化します。</span><span class="sxs-lookup"><span data-stu-id="752f4-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="752f4-144">これは、[out] の情報です。</span><span class="sxs-lookup"><span data-stu-id="752f4-144">This is the [out] information.</span></span> <span data-ttu-id="752f4-145">状態になっている間、クライアントは、その状態に対応するデータ構造を更新します。</span><span class="sxs-lookup"><span data-stu-id="752f4-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="752f4-146">これは [入力] 情報です。</span><span class="sxs-lookup"><span data-stu-id="752f4-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="752f4-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="752f4-147">See also</span></span>



[<span data-ttu-id="752f4-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="752f4-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="752f4-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="752f4-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="752f4-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="752f4-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="752f4-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="752f4-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="752f4-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="752f4-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="752f4-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="752f4-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="752f4-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="752f4-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="752f4-155">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="752f4-155">MAPI Constants</span></span>](mapi-constants.md)

