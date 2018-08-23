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
ms.openlocfilehash: 07305f712fd925b206ce18a32f8f5a24f199ccbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801084"
---
# <a name="iostxinitsync"></a><span data-ttu-id="77d8c-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="77d8c-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="77d8c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77d8c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77d8c-105">同期を開始しようとしていますが、ローカル メッセージ ストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="77d8c-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="77d8c-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="77d8c-106">Parameters</span></span>

 <span data-ttu-id="77d8c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="77d8c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="77d8c-108">[in]同期中に、適切な動作を決定するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="77d8c-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="77d8c-109">Outlook は、クライアントに提供する情報を決定するのにレプリケーションの状態マシンの各状態でこれらのフラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="77d8c-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="77d8c-110">たとえば、クライアントでは、 **SYNC_ONLY_ASSOCIATED**が成功した場合 Outlook はのみを返す関連付けられている (非表示) の項目に関連する情報です。</span><span class="sxs-lookup"><span data-stu-id="77d8c-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="77d8c-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="77d8c-111">See also</span></span>



[<span data-ttu-id="77d8c-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="77d8c-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="77d8c-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="77d8c-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="77d8c-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="77d8c-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="77d8c-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="77d8c-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="77d8c-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="77d8c-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="77d8c-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="77d8c-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="77d8c-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77d8c-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="77d8c-119">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="77d8c-119">MAPI Constants</span></span>](mapi-constants.md)

