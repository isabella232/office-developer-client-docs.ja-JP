---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 78ccf72f17ec350d77f2d22d0e6d2fa7c3d97543
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432871"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="54ee8-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="54ee8-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="54ee8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54ee8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54ee8-105">同期の結果を設定します。</span><span class="sxs-lookup"><span data-stu-id="54ee8-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="54ee8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="54ee8-106">Parameters</span></span>

 <span data-ttu-id="54ee8-107">_hrsync_</span><span class="sxs-lookup"><span data-stu-id="54ee8-107">_hrSync_</span></span>
  
>  <span data-ttu-id="54ee8-108">順番同期の結果。</span><span class="sxs-lookup"><span data-stu-id="54ee8-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54ee8-109">注釈</span><span class="sxs-lookup"><span data-stu-id="54ee8-109">Remarks</span></span>

<span data-ttu-id="54ee8-110">同期の結果をローカルストアに通知するには、iostx:: **syncend**を呼び出す前に、 **iostx:: SetSyncResult**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="54ee8-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54ee8-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="54ee8-111">See also</span></span>



[<span data-ttu-id="54ee8-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="54ee8-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="54ee8-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="54ee8-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="54ee8-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="54ee8-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="54ee8-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="54ee8-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="54ee8-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="54ee8-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="54ee8-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="54ee8-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="54ee8-118">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="54ee8-118">MAPI Constants</span></span>](mapi-constants.md)

