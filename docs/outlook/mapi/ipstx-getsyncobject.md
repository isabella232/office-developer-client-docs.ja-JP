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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315086"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="0c675-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="0c675-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="0c675-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c675-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c675-105">同期セッションを開始し、関連付けられた**[iostx](iostxiunknown.md)** インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="0c675-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="0c675-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c675-106">Parameters</span></span>

 <span data-ttu-id="0c675-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="0c675-107">_ppostx_</span></span>
  
>  <span data-ttu-id="0c675-108">読み上げ取得する**iostx**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c675-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c675-109">解説</span><span class="sxs-lookup"><span data-stu-id="0c675-109">Remarks</span></span>

<span data-ttu-id="0c675-110">呼び出し元は、同じフォルダーが複数のスレッドで同時に同期されないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c675-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c675-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c675-111">See also</span></span>



[<span data-ttu-id="0c675-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="0c675-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="0c675-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0c675-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

