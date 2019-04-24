---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341021"
---
# <a name="fbadrowset"></a><span data-ttu-id="90ade-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="90ade-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="90ade-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90ade-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90ade-105">テーブルの行のセットに含まれるすべてのテーブルの行を検証します。</span><span class="sxs-lookup"><span data-stu-id="90ade-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90ade-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="90ade-106">Header file:</span></span>  <br/> |<span data-ttu-id="90ade-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="90ade-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="90ade-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="90ade-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="90ade-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="90ade-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="90ade-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="90ade-110">Called by:</span></span>  <br/> |<span data-ttu-id="90ade-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="90ade-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="90ade-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="90ade-112">Parameters</span></span>

 <span data-ttu-id="90ade-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="90ade-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="90ade-114">順番検証する行セットを識別する[srowset](srowset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="90ade-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="90ade-115">ポインターが NULL の場合、この構造体は無効です。</span><span class="sxs-lookup"><span data-stu-id="90ade-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="90ade-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="90ade-116">Return value</span></span>

<span data-ttu-id="90ade-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="90ade-117">TRUE</span></span> 
  
> <span data-ttu-id="90ade-118">指定された行セットの行が無効であるか、行セット自体が無効です。</span><span class="sxs-lookup"><span data-stu-id="90ade-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="90ade-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="90ade-119">FALSE</span></span> 
  
> <span data-ttu-id="90ade-120">指定した行セットと行セット自体の行はすべて有効です。</span><span class="sxs-lookup"><span data-stu-id="90ade-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90ade-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="90ade-121">See also</span></span>



[<span data-ttu-id="90ade-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="90ade-122">FBadRow</span></span>](fbadrow.md)

