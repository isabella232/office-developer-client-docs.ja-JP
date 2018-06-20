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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801095"
---
# <a name="iostxsyncend"></a><span data-ttu-id="23e03-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="23e03-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="23e03-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23e03-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23e03-105">現在の状態で同期を終了し、その状態を終了します。</span><span class="sxs-lookup"><span data-stu-id="23e03-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="23e03-106">備考</span><span class="sxs-lookup"><span data-stu-id="23e03-106">Remarks</span></span>

<span data-ttu-id="23e03-107">クライアントは、 [IOSTX::SyncBeg](iostx-syncbeg.md)を呼び出すたびに**IOSTX::SyncEnd**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="23e03-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="23e03-108">対応するデータ構造は、クライアントが Outlook では、内部の状態をクリーンアップできるように現在の状態を完了正常にかどうかを示す情報を保持します。</span><span class="sxs-lookup"><span data-stu-id="23e03-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23e03-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="23e03-109">See also</span></span>



[<span data-ttu-id="23e03-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="23e03-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="23e03-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="23e03-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="23e03-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="23e03-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="23e03-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="23e03-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="23e03-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="23e03-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="23e03-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="23e03-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="23e03-116">IOSTX: IUnknown</span><span class="sxs-lookup"><span data-stu-id="23e03-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="23e03-117">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="23e03-117">MAPI Constants</span></span>](mapi-constants.md)

