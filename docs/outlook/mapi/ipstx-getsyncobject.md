---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407110"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="89e49-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="89e49-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="89e49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89e49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89e49-105">同期セッションを開始し、関連付けられた **[IOSTX インターフェイスを取得](iostxiunknown.md)** します。</span><span class="sxs-lookup"><span data-stu-id="89e49-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="89e49-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89e49-106">Parameters</span></span>

 <span data-ttu-id="89e49-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="89e49-107">_ppostx_</span></span>
  
>  <span data-ttu-id="89e49-108">[out]取得する **IOSTX** インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="89e49-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="89e49-109">注釈</span><span class="sxs-lookup"><span data-stu-id="89e49-109">Remarks</span></span>

<span data-ttu-id="89e49-110">呼び出し元は、同じフォルダーが複数のスレッドで同時に同期されない必要があります。</span><span class="sxs-lookup"><span data-stu-id="89e49-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="89e49-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="89e49-111">See also</span></span>



[<span data-ttu-id="89e49-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="89e49-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="89e49-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="89e49-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

