---
title: '[RelQuadBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: 図形の幅と高さに相対する2次ベジエ曲線の x 座標と y 座標、および図形の幅と高さに相対する曲線のコントロールポイントの x 座標と y 座標を格納します。
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319930"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="d4e71-103">[RelQuadBezTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="d4e71-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="d4e71-104">図形の幅と高さに相対する2次ベジエ曲線の*x*座標と*y*座標、および図形の幅と高さに相対する曲線のコントロールポイントの*x*座標と*y*座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="d4e71-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d4e71-105">[**RelQuadBezTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。</span><span class="sxs-lookup"><span data-stu-id="d4e71-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="d4e71-106">Visio 2003-2010 形式でファイルを保存すると、 **[relquadbezto]** 行は[[nurbsto]](nurbsto-row-geometry-section.md)の行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="d4e71-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="d4e71-107">[**RelQuadBezTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d4e71-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="d4e71-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d4e71-108">**Cell**</span></span>|<span data-ttu-id="d4e71-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="d4e71-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4e71-110">X</span><span class="sxs-lookup"><span data-stu-id="d4e71-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="d4e71-111">図形の幅を基準にして、2次ベジエ曲線の最後の頂点に対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="d4e71-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="d4e71-112">Y</span><span class="sxs-lookup"><span data-stu-id="d4e71-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="d4e71-113">図形の高さを基準にした、2次ベジエ曲線の最後の頂点に対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="d4e71-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="d4e71-114">A</span><span class="sxs-lookup"><span data-stu-id="d4e71-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="d4e71-115">図形の幅を基準にして、曲線のコントロールポイントの*x*座標を指定します。弧の点を指定します。コントロールポイントは、円弧の始点と終点の間の中間点を中心に配置されます。</span><span class="sxs-lookup"><span data-stu-id="d4e71-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="d4e71-116">B</span><span class="sxs-lookup"><span data-stu-id="d4e71-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="d4e71-117">図形の高さを基準にして、曲線のコントロールポイントの*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="d4e71-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

