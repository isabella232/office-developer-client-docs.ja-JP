---
title: '[RelCubBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: 図形の幅と高さを基準にした 3 次ベジエ曲線の端点の x 座標と y 座標、曲線の幅と高さの先頭のコントロール ポイントの x 座標と y 座標、および曲線相対図形の幅と高さの終了のコントロール ポイントの x 座標と y 座標を格納します。
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430330"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="869d7-103">[RelCubBezTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="869d7-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="869d7-104">図形の幅と高さを基準にした 3 次ベジエ曲線の端点の x 座標と *y* 座標、曲線の幅と高さの先頭のコントロール ポイントの x 座標と y 座標、および曲線相対図形の幅と高さの終了のコントロール ポイントの *x* 座標と *y* 座標を格納します。 </span><span class="sxs-lookup"><span data-stu-id="869d7-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="869d7-105">[**RelCubBezTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。</span><span class="sxs-lookup"><span data-stu-id="869d7-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="869d7-106">ファイルを Visio 2003- 2010 形式に保存すると **、RelCubBezTo** 行は [NURBSTo](nurbsto-row-geometry-section.md)行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="869d7-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="869d7-107">[**RelCubBezTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="869d7-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="869d7-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="869d7-108">**Cell**</span></span>|<span data-ttu-id="869d7-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="869d7-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="869d7-110">X</span><span class="sxs-lookup"><span data-stu-id="869d7-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="869d7-111">図形  *の*  幅に対する 3 次ベジエ曲線の終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="869d7-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="869d7-112">Y</span><span class="sxs-lookup"><span data-stu-id="869d7-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="869d7-113">図形  *の高*  さに対する 3 次ベジエ曲線の終了頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="869d7-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="869d7-114">A</span><span class="sxs-lookup"><span data-stu-id="869d7-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="869d7-115">図形  *の*  幅に対する曲線の開始コントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始頂点と終了頂点の間に最適です。</span><span class="sxs-lookup"><span data-stu-id="869d7-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="869d7-116">B</span><span class="sxs-lookup"><span data-stu-id="869d7-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="869d7-117">図形  *の高*  さを基準にした曲線の開始コントロール ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="869d7-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="869d7-118">C</span><span class="sxs-lookup"><span data-stu-id="869d7-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="869d7-119">図形  *の*  幅に対する曲線の終了コントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始コントロール ポイントと終了頂点の間に最適です。</span><span class="sxs-lookup"><span data-stu-id="869d7-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="869d7-120">D</span><span class="sxs-lookup"><span data-stu-id="869d7-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="869d7-121">図形  *の高*  さを基準にした曲線の終了コントロール ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="869d7-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

