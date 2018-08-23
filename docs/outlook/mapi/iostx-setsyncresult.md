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
ms.openlocfilehash: f8982bafc0678378ae46dc31a9417cc11bb695a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563073"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="0d1b0-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="0d1b0-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="0d1b0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d1b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d1b0-105">同期の結果を設定します。</span><span class="sxs-lookup"><span data-stu-id="0d1b0-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="0d1b0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d1b0-106">Parameters</span></span>

 <span data-ttu-id="0d1b0-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="0d1b0-107">_hrSync_</span></span>
  
>  <span data-ttu-id="0d1b0-108">[in]同期の結果を返します。</span><span class="sxs-lookup"><span data-stu-id="0d1b0-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0d1b0-109">注釈</span><span class="sxs-lookup"><span data-stu-id="0d1b0-109">Remarks</span></span>

<span data-ttu-id="0d1b0-110">ローカル ストアの同期の結果を通知するために**IOSTX::SyncEnd**を呼び出す前に**IOSTX::SetSyncResult**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0d1b0-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0d1b0-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d1b0-111">See also</span></span>



[<span data-ttu-id="0d1b0-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0d1b0-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="0d1b0-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="0d1b0-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="0d1b0-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="0d1b0-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="0d1b0-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="0d1b0-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="0d1b0-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="0d1b0-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="0d1b0-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="0d1b0-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="0d1b0-118">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="0d1b0-118">MAPI Constants</span></span>](mapi-constants.md)

