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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429349"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="9db44-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="9db44-103">SizedSPropTagArray</span></span>

<span data-ttu-id="9db44-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9db44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9db44-105">指定した数の [プロパティ タグを含む名前付き SPropTagArray](sproptagarray.md) 構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="9db44-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9db44-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9db44-106">Header file:</span></span>  <br/> |<span data-ttu-id="9db44-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9db44-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9db44-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="9db44-108">Related structure:</span></span>  <br/> |<span data-ttu-id="9db44-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="9db44-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="9db44-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9db44-110">Parameters</span></span>

<span data-ttu-id="9db44-111">_ _ctag_</span><span class="sxs-lookup"><span data-stu-id="9db44-111">_ _ctag_</span></span>
  
> <span data-ttu-id="9db44-112">新しい構造に含めるプロパティ タグの数。</span><span class="sxs-lookup"><span data-stu-id="9db44-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="9db44-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="9db44-113">_ _name_</span></span>
  
> <span data-ttu-id="9db44-114">新しい構造の名前。</span><span class="sxs-lookup"><span data-stu-id="9db44-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9db44-115">注釈</span><span class="sxs-lookup"><span data-stu-id="9db44-115">Remarks</span></span>

<span data-ttu-id="9db44-116">**SizedSPropTagArray** マクロを使用して、明示的な境界を持つプロパティ タグ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="9db44-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="9db44-117">**SizedSPropTagArray** マクロから得られた新しい構造を **SPropTagArray** 構造体へのポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="9db44-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="9db44-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="9db44-118">See also</span></span>

- [<span data-ttu-id="9db44-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="9db44-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="9db44-120">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="9db44-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

