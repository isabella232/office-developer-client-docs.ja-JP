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
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="6e034-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="6e034-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="6e034-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e034-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e034-105">同期セッションを開始し、関連付けられている**[IOSTX](iostxiunknown.md)** インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="6e034-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="6e034-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e034-106">Parameters</span></span>

 <span data-ttu-id="6e034-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="6e034-107">_ppostx_</span></span>
  
>  <span data-ttu-id="6e034-108">[out]取得する**IOSTX**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6e034-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6e034-109">備考</span><span class="sxs-lookup"><span data-stu-id="6e034-109">Remarks</span></span>

<span data-ttu-id="6e034-110">呼び出し元は、同じフォルダーが 2 つ以上のスレッドで同時に同期されていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e034-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e034-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e034-111">See also</span></span>



[<span data-ttu-id="6e034-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="6e034-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="6e034-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6e034-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

