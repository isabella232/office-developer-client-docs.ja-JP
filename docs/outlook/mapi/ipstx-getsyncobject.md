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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801196"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="d8ca3-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="d8ca3-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="d8ca3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8ca3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8ca3-105">同期セッションを開始し、関連付けられている**[IOSTX](iostxiunknown.md)** インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d8ca3-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="d8ca3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d8ca3-106">Parameters</span></span>

 <span data-ttu-id="d8ca3-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="d8ca3-107">_ppostx_</span></span>
  
>  <span data-ttu-id="d8ca3-108">[out]取得する**IOSTX**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d8ca3-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d8ca3-109">注釈</span><span class="sxs-lookup"><span data-stu-id="d8ca3-109">Remarks</span></span>

<span data-ttu-id="d8ca3-110">呼び出し元は、同じフォルダーが 2 つ以上のスレッドで同時に同期されていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8ca3-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8ca3-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8ca3-111">See also</span></span>



[<span data-ttu-id="d8ca3-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="d8ca3-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="d8ca3-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d8ca3-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

