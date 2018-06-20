---
title: '[RelEllipticalArcTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: 含まれています x と y の図形の幅と高さ、x を基準にして楕円の円弧の端点の座標および y-図形の幅と高さを基準にして円弧のコントロール ポイントの座標が x の角度、楕円の長軸、および t の比率を軸彼は楕円の長軸と短軸の軸。
ms.openlocfilehash: 417a2a92bc5c94f9620c7c6f1081ba81d93aa890
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806185"
---
# <a name="relellipticalarcto-row-geometry-section"></a><span data-ttu-id="cb40b-103">[RelEllipticalArcTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="cb40b-103">RelEllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="cb40b-104">*X*と*y* - 図形の幅と高さ、 *x*を基準にして楕円の円弧の端点の座標と*y*が含まれていますが、図形の幅と高さを基準にして円弧のコントロール ポイントの座標が*x*の角度  軸には、楕円の長軸、および楕円の長軸と短軸の軸との比率です。</span><span class="sxs-lookup"><span data-stu-id="cb40b-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint relative to the shape's width and height,  *x*  - and  *y*  -coordinates of the control points on the arc relative to the shape's width and height, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cb40b-105">**RelEllipticalArcTo**行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保持できます。</span><span class="sxs-lookup"><span data-stu-id="cb40b-105">A **RelEllipticalArcTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="cb40b-106">Visio 2003 から 2010 年の形式にファイルを保存すると、 **RelEllipticalArcTo**行が[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)の行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="cb40b-106">When a file is saved to the Visio 2003-2010 formats, the **RelEllipticalArcTo** row is converted to an [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="cb40b-107">**RelEllipticalArcTo**行には、次のセルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb40b-107">A **RelEllipticalArcTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="cb40b-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="cb40b-108">**Cell**</span></span>|<span data-ttu-id="cb40b-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb40b-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb40b-110">X</span><span class="sxs-lookup"><span data-stu-id="cb40b-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="cb40b-111">*X* -図形の幅を基準にして円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="cb40b-111">The  *x*  -coordinate of the ending vertex on an arc relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="cb40b-112">Y</span><span class="sxs-lookup"><span data-stu-id="cb40b-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="cb40b-113">*Y* -図形の高さを基準にして円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="cb40b-113">The  *y*  -coordinate of the ending vertex on an arc relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="cb40b-114">A</span><span class="sxs-lookup"><span data-stu-id="cb40b-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="cb40b-115">*X* -図形の幅を基準にして、円弧のコントロール ポイントの座標円弧上の点。コントロール ポイントは、最初と最後の円弧の頂点の間で途中で最適に配置します。それ以外の場合、円弧は、予期しない結果で、コントロール ポイントを通過するために極端になることがあります。</span><span class="sxs-lookup"><span data-stu-id="cb40b-115">The  *x*  -coordinate of the arc's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="cb40b-116">B</span><span class="sxs-lookup"><span data-stu-id="cb40b-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="cb40b-117">*Y* -図形の幅を基準にして、円弧のコントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="cb40b-117">The  *y*  -coordinate of an arc's control point relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="cb40b-118">C</span><span class="sxs-lookup"><span data-stu-id="cb40b-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="cb40b-119">*X*を基準にして、円弧の長軸の角度を親の軸です。</span><span class="sxs-lookup"><span data-stu-id="cb40b-119">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="cb40b-120">D</span><span class="sxs-lookup"><span data-stu-id="cb40b-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="cb40b-p102">円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cb40b-p102">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb40b-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="cb40b-124">Remarks</span></span>

<span data-ttu-id="cb40b-125">**RelEllipticalArcTo**行の値は、 [EllipticalArcTo](ellipticalarcto-row-geometry-section.md)行、図形の高さと幅を掛けた値に相当します。</span><span class="sxs-lookup"><span data-stu-id="cb40b-125">Values in the **RelEllipticalArcTo** row are equivalent to values in an [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) row, multiplied by the width and height of the shape.</span></span> <span data-ttu-id="cb40b-126">たとえば: **RelEllipticalArcTo**行の**X**、 **Y**、 **A**、 **B** **C**および**D**のセルが値を持つ、1、1、1.5、0.5 15 度、および 1.5 (それぞれ) と交換できます**EllipticalArcTo**行セルの数式`Width*1`、 `Height*1'`、 `Width*1.5`、 `Height*0.5`、15 度、および 1.5 (それぞれ)。</span><span class="sxs-lookup"><span data-stu-id="cb40b-126">For example: a **RelEllipticalArcTo** row where the **X**, **Y**, **A**, **B**, **C**, and **D** cells have the values 1, 1, 1.5, 0.5, 15 deg, and 1.5 (respectively) can be replaced with an **EllipticalArcTo** row with the cell formulas  `Width*1`,  `Height*1'`,  `Width*1.5`,  `Height*0.5`, 15 deg, and 1.5 (respectively).</span></span>
  

