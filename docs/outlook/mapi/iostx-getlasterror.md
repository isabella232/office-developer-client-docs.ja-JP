---
title: iostxgetlasterror
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9c29011ae2e9b59a7a0a38148fa6c5b673fd9590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422300"
---
# <a name="iostxgetlasterror"></a><span data-ttu-id="2a02d-103">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2a02d-103">IOSTX::GetLastError</span></span>

  
  
<span data-ttu-id="2a02d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a02d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a02d-105">最新のエラーに関する拡張情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="2a02d-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="2a02d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2a02d-106">Parameters</span></span>

 <span data-ttu-id="2a02d-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="2a02d-107">_hResult_</span></span>
  
>  <span data-ttu-id="2a02d-108">順番エラーコード。</span><span class="sxs-lookup"><span data-stu-id="2a02d-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="2a02d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2a02d-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="2a02d-110">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="2a02d-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="2a02d-111">これは0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a02d-111">This must be 0.</span></span> 
    
 <span data-ttu-id="2a02d-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="2a02d-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="2a02d-113">読み上げエラーの拡張情報を含む**MAPIERROR**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2a02d-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="2a02d-114">**LPMAPIERROR**の型定義については、「mapidefs.h」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a02d-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2a02d-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a02d-115">See also</span></span>



[<span data-ttu-id="2a02d-116">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="2a02d-116">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="2a02d-117">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="2a02d-117">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="2a02d-118">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="2a02d-118">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="2a02d-119">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="2a02d-119">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="2a02d-120">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="2a02d-120">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="2a02d-121">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="2a02d-121">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="2a02d-122">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2a02d-122">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="2a02d-123">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="2a02d-123">MAPI Constants</span></span>](mapi-constants.md)

