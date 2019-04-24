---
title: '[NURBSTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251758
localization_priority: Normal
ms.assetid: 7e47acfe-5ec0-3689-eb89-0168f596a739
description: x 座標と y 座標、2番目から最後のノットの位置、最後の太さの位置、最初のノットの位置、最初の太さの位置、および不均一な有理数 B-スプライン (NURBS) の数式を格納します。
ms.openlocfilehash: a5fc83f9581277580d076c2a850bfe937602aef0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361020"
---
# <a name="nurbsto-row-geometry-section"></a><span data-ttu-id="53335-103">[NURBSTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="53335-103">NURBSTo Row (Geometry Section)</span></span>

<span data-ttu-id="53335-104">*x*座標と*y*座標、2番目から最後のノットの位置、最後の太さの位置、最初のノットの位置、最初の太さの位置、および不均一な有理数 B-スプライン (NURBS) の数式を格納します。</span><span class="sxs-lookup"><span data-stu-id="53335-104">Contains the  *x*  - and  *y*  -coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, and the formula for a nonuniform rational B-spline (NURBS).</span></span> 
  
<span data-ttu-id="53335-105">[NURBSTo] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="53335-105">A NURBSTo row contains the following cells.</span></span>
  
|<span data-ttu-id="53335-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="53335-106">**Cell**</span></span>|<span data-ttu-id="53335-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="53335-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53335-108">X</span><span class="sxs-lookup"><span data-stu-id="53335-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="53335-109">NURBS の最後のコントロールポイントに対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="53335-109">The  *x*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="53335-110">Y</span><span class="sxs-lookup"><span data-stu-id="53335-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="53335-111">NURBS の最後のコントロールポイントに対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="53335-111">The  *y*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="53335-112">A</span><span class="sxs-lookup"><span data-stu-id="53335-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="53335-113">NURBS の最後から 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="53335-113">The second to the last knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="53335-114">B</span><span class="sxs-lookup"><span data-stu-id="53335-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="53335-115">NURBS の最後のウェイトです。</span><span class="sxs-lookup"><span data-stu-id="53335-115">The last weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="53335-116">C</span><span class="sxs-lookup"><span data-stu-id="53335-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="53335-117">NURBS の最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="53335-117">The first knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="53335-118">D</span><span class="sxs-lookup"><span data-stu-id="53335-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="53335-119">NURBS の最初のウェイトです。</span><span class="sxs-lookup"><span data-stu-id="53335-119">The first weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="53335-120">E</span><span class="sxs-lookup"><span data-stu-id="53335-120">E</span></span>](e-cell-geometry-section.md) <br/> |<span data-ttu-id="53335-121">NURBS の数式です。</span><span class="sxs-lookup"><span data-stu-id="53335-121">A NURBS formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53335-122">解説</span><span class="sxs-lookup"><span data-stu-id="53335-122">Remarks</span></span>

<span data-ttu-id="53335-p101">NURBS は曲線を数理的に表すための一般的な方法です。**[自在曲線ツール]** を使用して、NURBS を作成できます。</span><span class="sxs-lookup"><span data-stu-id="53335-p101">NURBS is a common way to represent a curve mathematically. You can create a NURBS with the **Freeform** tool.</span></span> 
  

