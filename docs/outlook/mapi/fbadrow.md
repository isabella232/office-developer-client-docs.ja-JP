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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800060"
---
# <a name="fbadrow"></a><span data-ttu-id="e01a8-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="e01a8-103">FBadRow</span></span>

  
  
<span data-ttu-id="e01a8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e01a8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e01a8-105">テーブル内の行を検証します。</span><span class="sxs-lookup"><span data-stu-id="e01a8-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e01a8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e01a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="e01a8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="e01a8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="e01a8-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e01a8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e01a8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e01a8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e01a8-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e01a8-110">Called by:</span></span>  <br/> |<span data-ttu-id="e01a8-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e01a8-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="e01a8-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e01a8-112">Parameters</span></span>

 <span data-ttu-id="e01a8-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="e01a8-113">_lprow_</span></span>
  
> <span data-ttu-id="e01a8-114">[in]検証する行を識別する[SRow](srow.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e01a8-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e01a8-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e01a8-115">Return value</span></span>

<span data-ttu-id="e01a8-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="e01a8-116">TRUE</span></span> 
  
> <span data-ttu-id="e01a8-117">指定された行が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="e01a8-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="e01a8-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="e01a8-118">FALSE</span></span> 
  
> <span data-ttu-id="e01a8-119">指定した行が無効です。</span><span class="sxs-lookup"><span data-stu-id="e01a8-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e01a8-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="e01a8-120">See also</span></span>



[<span data-ttu-id="e01a8-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="e01a8-121">FBadRowSet</span></span>](fbadrowset.md)

