---
title: CbNewSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CbNewSSortOrderSet
api_type:
- COM
ms.assetid: a2fb67e0-ccdb-4eb0-9f8c-75213442159f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a9d01d3b8d414032d0d4f05fe5f966640a181ba1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317956"
---
# <a name="cbnewssortorderset"></a><span data-ttu-id="f937c-103">CbNewSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="f937c-103">CbNewSSortOrderSet</span></span>

  
  
<span data-ttu-id="f937c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f937c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f937c-105">sorderstructure で表される、指定された数の並べ替え順序を含む新しい[sizedssortorderset](sizedssortorderset.md)構造体に割り当てる[](ssortorder.md)バイト数を計算します。</span><span class="sxs-lookup"><span data-stu-id="f937c-105">Computes the number of bytes to be allocated for a new [SizedSSortOrderSet](sizedssortorderset.md) structure that contains a specified number of sort orders represented by [SSortOrder](ssortorder.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f937c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f937c-106">Header file:</span></span>  <br/> |<span data-ttu-id="f937c-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f937c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f937c-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="f937c-108">Related structure:</span></span>  <br/> |<span data-ttu-id="f937c-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="f937c-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
CbNewSSortOrderSet (_csort)
```

## <a name="parameters"></a><span data-ttu-id="f937c-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f937c-110">Parameters</span></span>

 <span data-ttu-id="f937c-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="f937c-111">__csort_</span></span>
  
> <span data-ttu-id="f937c-112">**ssortorderset**構造に含める、sorderstructure の数。 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f937c-112">Count of **SSortOrder** structures to be included in the **SSortOrderSet** structure.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f937c-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="f937c-113">See also</span></span>



[<span data-ttu-id="f937c-114">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="f937c-114">SizedSSortOrderSet</span></span>](sizedssortorderset.md)
  
[<span data-ttu-id="f937c-115">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="f937c-115">SSortOrder</span></span>](ssortorder.md)


[<span data-ttu-id="f937c-116">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="f937c-116">Macros Related to Structures</span></span>](macros-related-to-structures.md)

