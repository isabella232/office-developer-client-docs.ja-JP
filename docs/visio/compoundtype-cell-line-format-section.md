---
title: '[CompoundType] セル ([線の形式] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: 図形の線の複合型を指定します。
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359371"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="7b112-103">[CompoundType] セル ([線の形式] セクション)</span><span class="sxs-lookup"><span data-stu-id="7b112-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="7b112-104">図形の線の複合型を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b112-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="7b112-105">**値**</span><span class="sxs-lookup"><span data-stu-id="7b112-105">**Value**</span></span>|<span data-ttu-id="7b112-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="7b112-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b112-107">.0</span><span class="sxs-lookup"><span data-stu-id="7b112-107">0</span></span>  <br/> |<span data-ttu-id="7b112-108">Simple/標準</span><span class="sxs-lookup"><span data-stu-id="7b112-108">Simple</span></span>  <br/> |
|<span data-ttu-id="7b112-109">1-d</span><span class="sxs-lookup"><span data-stu-id="7b112-109">1</span></span>  <br/> |<span data-ttu-id="7b112-110">倍精度浮動小数点数</span><span class="sxs-lookup"><span data-stu-id="7b112-110">Double</span></span>  <br/> |
|<span data-ttu-id="7b112-111">pbm-2</span><span class="sxs-lookup"><span data-stu-id="7b112-111">2</span></span>  <br/> |<span data-ttu-id="7b112-112">太線 (細)</span><span class="sxs-lookup"><span data-stu-id="7b112-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="7b112-113">1/3</span><span class="sxs-lookup"><span data-stu-id="7b112-113">3</span></span>  <br/> |<span data-ttu-id="7b112-114">細い太線</span><span class="sxs-lookup"><span data-stu-id="7b112-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="7b112-115">2/4</span><span class="sxs-lookup"><span data-stu-id="7b112-115">4</span></span>  <br/> |<span data-ttu-id="7b112-116">Triple</span><span class="sxs-lookup"><span data-stu-id="7b112-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b112-117">解説</span><span class="sxs-lookup"><span data-stu-id="7b112-117">Remarks</span></span>

<span data-ttu-id="7b112-118">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[compoundtype]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7b112-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b112-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="7b112-119">Cell name:</span></span>  <br/> | <span data-ttu-id="7b112-120">[compoundtype]</span><span class="sxs-lookup"><span data-stu-id="7b112-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="7b112-121">プログラムから、インデックスによって [ **[compoundtype]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b112-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b112-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7b112-122">Section index:</span></span>  <br/> |<span data-ttu-id="7b112-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7b112-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7b112-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7b112-124">Row index:</span></span>  <br/> |<span data-ttu-id="7b112-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="7b112-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="7b112-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7b112-126">Cell index:</span></span>  <br/> |<span data-ttu-id="7b112-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="7b112-127">**visCompoundType**</span></span> <br/> |
   

