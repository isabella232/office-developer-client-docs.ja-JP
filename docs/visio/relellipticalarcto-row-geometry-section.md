---
title: '[RelEllipticalArcTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: 図形の幅と高さを基準にした楕円弧の端点の x 座標および y 座標、図形の幅と高さに相対する円弧のコントロールポイントの x 座標と y 座標、x 軸から楕円の長軸までの角度、および t 間の比率を格納します。楕円の長軸と短軸。
ms.openlocfilehash: e38f5f2baf6bb9ade31c2778799a3ece968147f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409098"
---
# <a name="relellipticalarcto-row-geometry-section"></a><span data-ttu-id="1f9cf-103">[RelEllipticalArcTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="1f9cf-103">RelEllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="1f9cf-104">図形\*\* の幅と高さに相対する楕円の弧の端点に対する x 座標と*y*座標、図形の幅と高さに相対する円弧のコントロールポイントの*x*座標および*y*座標、および*x*からの角度を含みます。  -楕円の主軸までの軸、および楕円の長軸と短軸との比率を示します。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint relative to the shape's width and height,  *x*  - and  *y*  -coordinates of the control points on the arc relative to the shape's width and height, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1f9cf-105">[**RelEllipticalArcTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-105">A **RelEllipticalArcTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="1f9cf-106">Visio 2003-2010 形式でファイルを保存すると、 **[relellipticalarcto]** 行は[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md)の行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-106">When a file is saved to the Visio 2003-2010 formats, the **RelEllipticalArcTo** row is converted to an [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="1f9cf-107">[**RelEllipticalArcTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-107">A **RelEllipticalArcTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="1f9cf-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1f9cf-108">**Cell**</span></span>|<span data-ttu-id="1f9cf-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="1f9cf-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f9cf-110">X</span><span class="sxs-lookup"><span data-stu-id="1f9cf-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="1f9cf-111">図形の幅を基準にして、円弧の最後の頂点に対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-111">The  *x*  -coordinate of the ending vertex on an arc relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="1f9cf-112">Y</span><span class="sxs-lookup"><span data-stu-id="1f9cf-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="1f9cf-113">図形の高さを基準にして、円弧の最後の頂点に対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-113">The  *y*  -coordinate of the ending vertex on an arc relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="1f9cf-114">A</span><span class="sxs-lookup"><span data-stu-id="1f9cf-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="1f9cf-115">図形の幅を基準にした円弧のコントロールポイントの*x*座標です。弧の点を指定します。コントロールポイントは、円弧の始点と終点の間の中間点を中心に配置されます。それ以外の場合、円弧はコントロールポイントを通過するために極端なサイズまで拡大することがあり、予期しない結果が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-115">The  *x*  -coordinate of the arc's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="1f9cf-116">B</span><span class="sxs-lookup"><span data-stu-id="1f9cf-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="1f9cf-117">図形の幅を基準にした円弧のコントロールポイントの*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-117">The  *y*  -coordinate of an arc's control point relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="1f9cf-118">C</span><span class="sxs-lookup"><span data-stu-id="1f9cf-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="1f9cf-119">親の*x*軸を基準にした円弧の主軸の角度。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-119">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="1f9cf-120">D</span><span class="sxs-lookup"><span data-stu-id="1f9cf-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="1f9cf-p102">円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-p102">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f9cf-124">注釈</span><span class="sxs-lookup"><span data-stu-id="1f9cf-124">Remarks</span></span>

<span data-ttu-id="1f9cf-125">[**RelEllipticalArcTo**] 行の値は、図形の幅と高さを乗算した [[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)] 行の値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-125">Values in the **RelEllipticalArcTo** row are equivalent to values in an [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) row, multiplied by the width and height of the shape.</span></span> <span data-ttu-id="1f9cf-126">例: **X**、 **Y**、 **a**、 **B**、 **C**、および**D**の各セルが値1、1、1.5、0.5、15 deg、1.5 (それぞれ) を持つ **[relellipticalarcto]** 行は、 **[ellipticalarcto]** の行で置き換えることができます。セル数式`Width*1`、 `Height*1'`、 `Width*1.5` `Height*0.5`、、15 deg、および 1.5 (それぞれ)。</span><span class="sxs-lookup"><span data-stu-id="1f9cf-126">For example: a **RelEllipticalArcTo** row where the **X**, **Y**, **A**, **B**, **C**, and **D** cells have the values 1, 1, 1.5, 0.5, 15 deg, and 1.5 (respectively) can be replaced with an **EllipticalArcTo** row with the cell formulas  `Width*1`,  `Height*1'`,  `Width*1.5`,  `Height*0.5`, 15 deg, and 1.5 (respectively).</span></span>
  

