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
description: x 座標と y 座標、2 番目から最後のノットの位置、最後の重み付け位置、最初のノットの位置、最初の重み付け位置、および非ユニフォーム有理 B スプライン (NURBS) の数式を格納します。
ms.openlocfilehash: a5fc83f9581277580d076c2a850bfe937602aef0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404716"
---
# <a name="nurbsto-row-geometry-section"></a><span data-ttu-id="0db4e-103">[NURBSTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="0db4e-103">NURBSTo Row (Geometry Section)</span></span>

<span data-ttu-id="0db4e-104">*x* 座標と *y* 座標、2 番目から最後のノットの位置、最後の重み付け位置、最初のノットの位置、最初の重み付け位置、および非ユニフォーム有理 B スプライン (NURBS) の数式を格納します。</span><span class="sxs-lookup"><span data-stu-id="0db4e-104">Contains the  *x*  - and  *y*  -coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, and the formula for a nonuniform rational B-spline (NURBS).</span></span> 
  
<span data-ttu-id="0db4e-105">[NURBSTo] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0db4e-105">A NURBSTo row contains the following cells.</span></span>
  
|<span data-ttu-id="0db4e-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="0db4e-106">**Cell**</span></span>|<span data-ttu-id="0db4e-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="0db4e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0db4e-108">X</span><span class="sxs-lookup"><span data-stu-id="0db4e-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="0db4e-109">*NURBS* の最後のコントロール ポイントの x 座標。</span><span class="sxs-lookup"><span data-stu-id="0db4e-109">The  *x*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="0db4e-110">Y</span><span class="sxs-lookup"><span data-stu-id="0db4e-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="0db4e-111">NURBS の最後のコントロール ポイントの  *y*  座標。</span><span class="sxs-lookup"><span data-stu-id="0db4e-111">The  *y*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="0db4e-112">A</span><span class="sxs-lookup"><span data-stu-id="0db4e-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="0db4e-113">NURBS の最後から 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="0db4e-113">The second to the last knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="0db4e-114">B</span><span class="sxs-lookup"><span data-stu-id="0db4e-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="0db4e-115">NURBS の最後のウェイトです。</span><span class="sxs-lookup"><span data-stu-id="0db4e-115">The last weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="0db4e-116">C</span><span class="sxs-lookup"><span data-stu-id="0db4e-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="0db4e-117">NURBS の最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="0db4e-117">The first knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="0db4e-118">D</span><span class="sxs-lookup"><span data-stu-id="0db4e-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="0db4e-119">NURBS の最初のウェイトです。</span><span class="sxs-lookup"><span data-stu-id="0db4e-119">The first weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="0db4e-120">E</span><span class="sxs-lookup"><span data-stu-id="0db4e-120">E</span></span>](e-cell-geometry-section.md) <br/> |<span data-ttu-id="0db4e-121">NURBS の数式です。</span><span class="sxs-lookup"><span data-stu-id="0db4e-121">A NURBS formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0db4e-122">注釈</span><span class="sxs-lookup"><span data-stu-id="0db4e-122">Remarks</span></span>

<span data-ttu-id="0db4e-p101">NURBS は曲線を数理的に表すための一般的な方法です。**[自在曲線ツール]** を使用して、NURBS を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0db4e-p101">NURBS is a common way to represent a curve mathematically. You can create a NURBS with the **Freeform** tool.</span></span> 
  

