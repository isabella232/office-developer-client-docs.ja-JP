---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420620"
---
# <a name="fbadrow"></a><span data-ttu-id="2ad7b-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="2ad7b-103">FBadRow</span></span>

  
  
<span data-ttu-id="2ad7b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ad7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ad7b-105">テーブル内の行を検証します。</span><span class="sxs-lookup"><span data-stu-id="2ad7b-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ad7b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2ad7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="2ad7b-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2ad7b-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2ad7b-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="2ad7b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ad7b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2ad7b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2ad7b-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2ad7b-110">Called by:</span></span>  <br/> |<span data-ttu-id="2ad7b-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2ad7b-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="2ad7b-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ad7b-112">Parameters</span></span>

 <span data-ttu-id="2ad7b-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="2ad7b-113">_lprow_</span></span>
  
> <span data-ttu-id="2ad7b-114">順番検証する行を識別する[srow](srow.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ad7b-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ad7b-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="2ad7b-115">Return value</span></span>

<span data-ttu-id="2ad7b-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ad7b-116">TRUE</span></span> 
  
> <span data-ttu-id="2ad7b-117">指定した行は無効です。</span><span class="sxs-lookup"><span data-stu-id="2ad7b-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="2ad7b-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="2ad7b-118">FALSE</span></span> 
  
> <span data-ttu-id="2ad7b-119">指定した行は有効です。</span><span class="sxs-lookup"><span data-stu-id="2ad7b-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ad7b-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ad7b-120">See also</span></span>



[<span data-ttu-id="2ad7b-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="2ad7b-121">FBadRowSet</span></span>](fbadrowset.md)

