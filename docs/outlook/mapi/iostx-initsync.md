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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413354"
---
# <a name="iostxinitsync"></a><span data-ttu-id="1cf28-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="1cf28-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="1cf28-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cf28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cf28-105">同期が始まるとローカル メッセージ ストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="1cf28-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="1cf28-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1cf28-106">Parameters</span></span>

 <span data-ttu-id="1cf28-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1cf28-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1cf28-108">[in]同期中の適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="1cf28-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="1cf28-109">Outlook状態マシンの各状態でこれらのフラグを使用して、クライアントに提供する必要がある情報を決定します。</span><span class="sxs-lookup"><span data-stu-id="1cf28-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="1cf28-110">たとえば、クライアントがファイルを渡 **SYNC_ONLY_ASSOCIATED、Outlook** 関連する (または非表示の) アイテムにのみ関連する情報が返されます。</span><span class="sxs-lookup"><span data-stu-id="1cf28-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1cf28-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cf28-111">See also</span></span>



[<span data-ttu-id="1cf28-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1cf28-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="1cf28-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="1cf28-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="1cf28-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="1cf28-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="1cf28-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="1cf28-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="1cf28-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="1cf28-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="1cf28-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="1cf28-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="1cf28-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cf28-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="1cf28-119">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="1cf28-119">MAPI Constants</span></span>](mapi-constants.md)

