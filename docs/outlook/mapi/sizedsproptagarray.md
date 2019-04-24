---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282699"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="20fe5-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="20fe5-103">SizedSPropTagArray</span></span>

<span data-ttu-id="20fe5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20fe5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20fe5-105">指定した数のプロパティタグを含む名前付きの[SPropTagArray](sproptagarray.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="20fe5-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20fe5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="20fe5-106">Header file:</span></span>  <br/> |<span data-ttu-id="20fe5-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20fe5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="20fe5-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="20fe5-108">Related structure:</span></span>  <br/> |<span data-ttu-id="20fe5-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="20fe5-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="20fe5-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20fe5-110">Parameters</span></span>

<span data-ttu-id="20fe5-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="20fe5-111">__ctag_</span></span>
  
> <span data-ttu-id="20fe5-112">新しい構造に含めるプロパティタグの数。</span><span class="sxs-lookup"><span data-stu-id="20fe5-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="20fe5-113">__名前_</span><span class="sxs-lookup"><span data-stu-id="20fe5-113">__name_</span></span>
  
> <span data-ttu-id="20fe5-114">新しい構造の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="20fe5-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20fe5-115">解説</span><span class="sxs-lookup"><span data-stu-id="20fe5-115">Remarks</span></span>

<span data-ttu-id="20fe5-116">**SizedSPropTagArray**マクロを使用して、明示的な境界を持つプロパティタグ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="20fe5-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="20fe5-117">**SizedSPropTagArray**マクロの結果として得られる新しい構造を**SPropTagArray**構造体へのポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="20fe5-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="20fe5-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="20fe5-118">See also</span></span>

- [<span data-ttu-id="20fe5-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="20fe5-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="20fe5-120">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="20fe5-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

