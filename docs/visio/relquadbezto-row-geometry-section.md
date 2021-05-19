---
title: '[RelQuadBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: 図形の幅と高さに対する 2 次ベジエ曲線の端点の x 座標と y 座標、および図形の幅と高さを基準にした曲線のコントロール ポイントの x 座標と y 座標を格納します。
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423357"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="2a65d-103">[RelQuadBezTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="2a65d-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="2a65d-104">図形の幅と高さに対する 2 次ベジエ曲線の端点の x 座標と *y* 座標、および図形の幅と高さを基準にした曲線のコントロール ポイントの *x* 座標と *y* 座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="2a65d-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2a65d-105">[**RelQuadBezTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。</span><span class="sxs-lookup"><span data-stu-id="2a65d-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="2a65d-106">ファイルを 2003 から 2010 の Visio 形式に保存すると **、RelQuadBezTo** 行は [NURBSTo](nurbsto-row-geometry-section.md)行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="2a65d-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="2a65d-107">[**RelQuadBezTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a65d-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="2a65d-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="2a65d-108">**Cell**</span></span>|<span data-ttu-id="2a65d-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="2a65d-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a65d-110">X</span><span class="sxs-lookup"><span data-stu-id="2a65d-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="2a65d-111">図形  *の*  幅に対する 2 次ベジエ曲線の終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="2a65d-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="2a65d-112">Y</span><span class="sxs-lookup"><span data-stu-id="2a65d-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="2a65d-113">図形  *の高*  さを基準にした 2 次ベジエ曲線の終了頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="2a65d-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="2a65d-114">A</span><span class="sxs-lookup"><span data-stu-id="2a65d-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="2a65d-115">図形  *の*  幅を基準にした曲線のコントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始頂点と終了頂点の約半分の位置に最適です。</span><span class="sxs-lookup"><span data-stu-id="2a65d-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="2a65d-116">B</span><span class="sxs-lookup"><span data-stu-id="2a65d-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="2a65d-117">図形  *の高*  さを基準にした曲線のコントロール ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="2a65d-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

