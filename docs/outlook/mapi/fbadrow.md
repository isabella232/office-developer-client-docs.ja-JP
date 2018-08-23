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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800060"
---
# <a name="fbadrow"></a><span data-ttu-id="60576-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="60576-103">FBadRow</span></span>

  
  
<span data-ttu-id="60576-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="60576-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="60576-105">テーブル内の行を検証します。</span><span class="sxs-lookup"><span data-stu-id="60576-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="60576-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="60576-106">Header file:</span></span>  <br/> |<span data-ttu-id="60576-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="60576-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="60576-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="60576-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="60576-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="60576-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="60576-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="60576-110">Called by:</span></span>  <br/> |<span data-ttu-id="60576-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="60576-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="60576-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="60576-112">Parameters</span></span>

 <span data-ttu-id="60576-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="60576-113">_lprow_</span></span>
  
> <span data-ttu-id="60576-114">[in]検証する行を識別する[SRow](srow.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="60576-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="60576-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="60576-115">Return value</span></span>

<span data-ttu-id="60576-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="60576-116">TRUE</span></span> 
  
> <span data-ttu-id="60576-117">指定された行が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="60576-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="60576-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="60576-118">FALSE</span></span> 
  
> <span data-ttu-id="60576-119">指定した行が無効です。</span><span class="sxs-lookup"><span data-stu-id="60576-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="60576-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="60576-120">See also</span></span>



[<span data-ttu-id="60576-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="60576-121">FBadRowSet</span></span>](fbadrowset.md)

