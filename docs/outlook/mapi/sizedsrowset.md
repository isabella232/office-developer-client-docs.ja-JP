---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410932"
---
# <a name="sizedsrowset"></a><span data-ttu-id="ac3f6-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="ac3f6-103">SizedSRowSet</span></span>

<span data-ttu-id="ac3f6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac3f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac3f6-105">指定した行数 [を含む名前付き SRowSet](srowset.md) 構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac3f6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ac3f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="ac3f6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac3f6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ac3f6-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="ac3f6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ac3f6-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="ac3f6-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="ac3f6-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ac3f6-110">Parameters</span></span>

<span data-ttu-id="ac3f6-111">_ _crow_</span><span class="sxs-lookup"><span data-stu-id="ac3f6-111">_ _crow_</span></span>
  
> <span data-ttu-id="ac3f6-112">新しい構造に含める行の数。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="ac3f6-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="ac3f6-113">_ _name_</span></span>
  
> <span data-ttu-id="ac3f6-114">新しい構造の名前。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac3f6-115">注釈</span><span class="sxs-lookup"><span data-stu-id="ac3f6-115">Remarks</span></span>

<span data-ttu-id="ac3f6-116">**SizedSRowSet** マクロから得られた新しい構造を **SRowSet** 構造体へのポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="ac3f6-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac3f6-117">See also</span></span>

- [<span data-ttu-id="ac3f6-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="ac3f6-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="ac3f6-119">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="ac3f6-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

