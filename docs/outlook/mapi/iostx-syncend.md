---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439577"
---
# <a name="iostxsyncend"></a><span data-ttu-id="04569-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="04569-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="04569-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04569-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04569-105">現在の状態で同期を終了し、その状態を終了します。</span><span class="sxs-lookup"><span data-stu-id="04569-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="04569-106">注釈</span><span class="sxs-lookup"><span data-stu-id="04569-106">Remarks</span></span>

<span data-ttu-id="04569-107">クライアントは **、IOSTX::SyncBeg** への各呼び出しに対して [IOSTX::SyncEnd を呼び出す必要があります](iostx-syncbeg.md)。</span><span class="sxs-lookup"><span data-stu-id="04569-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="04569-108">対応するデータ構造には、クライアントが現在の状態を正常に完了したかどうかを示す情報が保持Outlook内部状態をクリーンアップできます。</span><span class="sxs-lookup"><span data-stu-id="04569-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04569-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="04569-109">See also</span></span>



[<span data-ttu-id="04569-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="04569-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="04569-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="04569-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="04569-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="04569-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="04569-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="04569-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="04569-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="04569-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="04569-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="04569-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="04569-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="04569-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="04569-117">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="04569-117">MAPI Constants</span></span>](mapi-constants.md)

