---
title: '[RelCubBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: X と y に対して、図形の幅と高さ、x の 3 次ベジエ曲線の端点の座標のとの曲線の相対的な図形の幅と高さ、および x の先頭のコントロール ポイントの座標の y と y の座標を移動するのl は、曲線の相対的な図形の幅と高さの最後のポイントです。
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806183"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="a72aa-103">[RelCubBezTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="a72aa-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="a72aa-104">*X*と*y*の基準にして図形の幅と高さ、 *x*の 3 次ベジエ曲線の端点の座標および*y*が含まれています-曲線の相対的な図形の幅と高さの最初の制御点の座標および*x*と*y*の曲線の相対的な図形の幅と高さの最後のコントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="a72aa-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a72aa-105">**RelCubBezTo**行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保持できます。</span><span class="sxs-lookup"><span data-stu-id="a72aa-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="a72aa-106">ファイル保存すると、Visio 2003 から 2010 年の書式には、 **RelCubBezTo**行が[[nurbsto]](nurbsto-row-geometry-section.md)行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="a72aa-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="a72aa-107">[**RelCubBezTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a72aa-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="a72aa-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a72aa-108">**Cell**</span></span>|<span data-ttu-id="a72aa-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="a72aa-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a72aa-110">X</span><span class="sxs-lookup"><span data-stu-id="a72aa-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a72aa-111">*X* -図形の幅を基準に、3 次ベジエ曲線の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="a72aa-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="a72aa-112">Y</span><span class="sxs-lookup"><span data-stu-id="a72aa-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a72aa-113">*Y* -図形の高さを基準にして、3 次ベジエ曲線の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="a72aa-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="a72aa-114">A</span><span class="sxs-lookup"><span data-stu-id="a72aa-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="a72aa-115">*X*の曲線の座標は図形の幅を基準にコントロール ポイントを開始の円弧上の点。コントロール ポイントは、最初と最後の円弧の頂点の間で置くが最適です。</span><span class="sxs-lookup"><span data-stu-id="a72aa-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="a72aa-116">B</span><span class="sxs-lookup"><span data-stu-id="a72aa-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="a72aa-117">*Y*の曲線の座標は、図形の高さを基準にコントロール ポイントを始めるのです。</span><span class="sxs-lookup"><span data-stu-id="a72aa-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="a72aa-118">C</span><span class="sxs-lookup"><span data-stu-id="a72aa-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="a72aa-119">*X*の曲線の座標に図形の幅を基準にコントロール ポイントの終了円弧上の点。コントロール ポイントは、円弧の先頭のコントロール ポイントおよび終了頂点の間で置くが最適です。</span><span class="sxs-lookup"><span data-stu-id="a72aa-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="a72aa-120">D</span><span class="sxs-lookup"><span data-stu-id="a72aa-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="a72aa-121">*Y*の座標の曲線の図形の高さを基準にコントロール ポイントを終了します。</span><span class="sxs-lookup"><span data-stu-id="a72aa-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

