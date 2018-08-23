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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5a0632ffd892c08fdf19de2c9b34607c27534f19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594041"
---
# <a name="iostxinitsync"></a><span data-ttu-id="d3909-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="d3909-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="d3909-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3909-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3909-105">同期を開始しようとしていますが、ローカル メッセージ ストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="d3909-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="d3909-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="d3909-106">Parameters</span></span>

 <span data-ttu-id="d3909-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3909-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d3909-108">[in]同期中に、適切な動作を決定するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3909-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="d3909-109">Outlook は、クライアントに提供する情報を決定するのにレプリケーションの状態マシンの各状態でこれらのフラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3909-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="d3909-110">たとえば、クライアントでは、 **SYNC_ONLY_ASSOCIATED**が成功した場合 Outlook はのみを返す関連付けられている (非表示) の項目に関連する情報です。</span><span class="sxs-lookup"><span data-stu-id="d3909-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d3909-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="d3909-111">See also</span></span>



[<span data-ttu-id="d3909-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d3909-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="d3909-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="d3909-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="d3909-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="d3909-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="d3909-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="d3909-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="d3909-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="d3909-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="d3909-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="d3909-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="d3909-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3909-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="d3909-119">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="d3909-119">MAPI Constants</span></span>](mapi-constants.md)

