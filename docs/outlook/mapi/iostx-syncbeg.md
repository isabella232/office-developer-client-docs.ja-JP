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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ddc61aa42b1087ed5f0ecb7986125ceef27cddce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801085"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="c901f-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="c901f-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="c901f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c901f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c901f-105">特定の状態の同期をローカル ストアを準備し、複製に必要な情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="c901f-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="c901f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c901f-106">Parameters</span></span>

 <span data-ttu-id="c901f-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="c901f-107">_uiSync_</span></span>
  
>  <span data-ttu-id="c901f-108">[in]ローカル ストアが入力されている状態です。</span><span class="sxs-lookup"><span data-stu-id="c901f-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="c901f-109">状態識別子の一覧は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c901f-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="c901f-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="c901f-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="c901f-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="c901f-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="c901f-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="c901f-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="c901f-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="c901f-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="c901f-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="c901f-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="c901f-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="c901f-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="c901f-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c901f-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="c901f-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="c901f-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="c901f-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="c901f-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="c901f-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="c901f-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="c901f-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="c901f-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="c901f-121">_ppv_</span><span class="sxs-lookup"><span data-stu-id="c901f-121">_ppv_</span></span>
  
>  <span data-ttu-id="c901f-122">[内] と [出力] を入力する状態に対応するデータ構造へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c901f-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="c901f-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="c901f-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="c901f-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="c901f-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="c901f-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="c901f-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="c901f-126">SYNC</span><span class="sxs-lookup"><span data-stu-id="c901f-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="c901f-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="c901f-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="c901f-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="c901f-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="c901f-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="c901f-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="c901f-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="c901f-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="c901f-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="c901f-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="c901f-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="c901f-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="c901f-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="c901f-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="c901f-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="c901f-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="c901f-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="c901f-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="c901f-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="c901f-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="c901f-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="c901f-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="c901f-138">注釈</span><span class="sxs-lookup"><span data-stu-id="c901f-138">Remarks</span></span>

<span data-ttu-id="c901f-139">クライアントでは、同期の結果を設定するのには**[IOSTX::SetSyncResult](iostx-setsyncresult.md)** を呼び出すし、その状態を終了するのには**[IOSTX::SyncEnd](iostx-syncend.md)** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c901f-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="c901f-140">クライアントは、状態が正常にレプリケートされたかどうかを判断するために**IOSTX::SyncBeg**が呼び出されるたびに、 **[IOSTX::SyncEnd](iostx-syncend.md)** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c901f-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="c901f-141">これが判明すると、Outlook の内部の状態をクリーンアップするのには開始できます。</span><span class="sxs-lookup"><span data-stu-id="c901f-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="c901f-142">[Out] これらの構造体の大部分が含まれている/[in] については、Outlook が Outlook に情報を渡すには、クライアント、およびクライアントに情報を渡すことを許可します。</span><span class="sxs-lookup"><span data-stu-id="c901f-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="c901f-143">クライアントは、 **IOSTX::SyncBeg**を呼び出して、Outlook は特定の状態のデータ構造体を割り当てるし、その状態の情報を初期化しています。</span><span class="sxs-lookup"><span data-stu-id="c901f-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="c901f-144">[Out] の情報です。</span><span class="sxs-lookup"><span data-stu-id="c901f-144">This is the [out] information.</span></span> <span data-ttu-id="c901f-145">、状態のときに、クライアントは、対応するデータ構造体をその状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="c901f-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="c901f-146">[In] これは、情報です。</span><span class="sxs-lookup"><span data-stu-id="c901f-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c901f-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="c901f-147">See also</span></span>



[<span data-ttu-id="c901f-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c901f-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="c901f-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="c901f-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="c901f-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="c901f-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="c901f-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="c901f-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="c901f-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="c901f-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="c901f-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="c901f-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="c901f-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c901f-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="c901f-155">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="c901f-155">MAPI Constants</span></span>](mapi-constants.md)

