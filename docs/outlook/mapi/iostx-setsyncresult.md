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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801086"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="d2012-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="d2012-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="d2012-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2012-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2012-105">同期の結果を設定します。</span><span class="sxs-lookup"><span data-stu-id="d2012-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="d2012-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d2012-106">Parameters</span></span>

 <span data-ttu-id="d2012-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="d2012-107">_hrSync_</span></span>
  
>  <span data-ttu-id="d2012-108">[in]同期の結果を返します。</span><span class="sxs-lookup"><span data-stu-id="d2012-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d2012-109">注釈</span><span class="sxs-lookup"><span data-stu-id="d2012-109">Remarks</span></span>

<span data-ttu-id="d2012-110">ローカル ストアの同期の結果を通知するために**IOSTX::SyncEnd**を呼び出す前に**IOSTX::SetSyncResult**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d2012-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2012-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2012-111">See also</span></span>



[<span data-ttu-id="d2012-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d2012-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="d2012-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="d2012-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="d2012-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="d2012-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="d2012-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="d2012-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="d2012-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="d2012-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="d2012-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="d2012-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="d2012-118">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="d2012-118">MAPI Constants</span></span>](mapi-constants.md)

