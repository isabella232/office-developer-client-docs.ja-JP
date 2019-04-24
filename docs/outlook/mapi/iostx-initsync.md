---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317193"
---
# <a name="iostxinitsync"></a><span data-ttu-id="22500-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="22500-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="22500-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22500-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22500-105">同期が開始されようとしていることをローカルメッセージストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="22500-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="22500-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="22500-106">Parameters</span></span>

 <span data-ttu-id="22500-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22500-107">_ulFlags_</span></span>
  
> <span data-ttu-id="22500-108">順番同期時に適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="22500-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="22500-109">Outlook は、レプリケーション状態マシンの各状態でこれらのフラグを使用して、クライアントに対して提供する必要のある情報を特定します。</span><span class="sxs-lookup"><span data-stu-id="22500-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="22500-110">たとえば、クライアントが**SYNC_ONLY_ASSOCIATED**に合格した場合、Outlook は関連付けられた (または非表示の) アイテムに関連する情報のみを返します。</span><span class="sxs-lookup"><span data-stu-id="22500-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="22500-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="22500-111">See also</span></span>



[<span data-ttu-id="22500-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="22500-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="22500-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="22500-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="22500-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="22500-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="22500-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="22500-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="22500-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="22500-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="22500-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="22500-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="22500-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22500-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="22500-119">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="22500-119">MAPI Constants</span></span>](mapi-constants.md)

