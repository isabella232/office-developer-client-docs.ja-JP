---
title: iostxsyncend
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332152"
---
# <a name="iostxsyncend"></a><span data-ttu-id="0ff39-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="0ff39-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="0ff39-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ff39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ff39-105">現在の状態で同期を終了し、その状態を終了します。</span><span class="sxs-lookup"><span data-stu-id="0ff39-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="0ff39-106">解説</span><span class="sxs-lookup"><span data-stu-id="0ff39-106">Remarks</span></span>

<span data-ttu-id="0ff39-107">[iostx:: SyncBeg](iostx-syncbeg.md)への呼び出しごとに、クライアントは**iostx:: syncend**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ff39-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="0ff39-108">対応するデータ構造には、Outlook が内部状態をクリーンアップできるように、クライアントが現在の状態を正常に完了したかどうかを示す情報が保持されます。</span><span class="sxs-lookup"><span data-stu-id="0ff39-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ff39-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ff39-109">See also</span></span>



[<span data-ttu-id="0ff39-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0ff39-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="0ff39-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="0ff39-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="0ff39-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="0ff39-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="0ff39-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="0ff39-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="0ff39-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="0ff39-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="0ff39-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="0ff39-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="0ff39-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ff39-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="0ff39-117">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="0ff39-117">MAPI Constants</span></span>](mapi-constants.md)

