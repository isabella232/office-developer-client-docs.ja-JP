---
title: '[RelEllipticalArcTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: 図形の幅と高さに対する楕円円弧の端点の x 座標と y 座標、図形の幅と高さに対する円弧上のコントロール ポイントの x 座標と y 座標、x 軸から楕円の長軸への角度、楕円の長軸と短軸の比率を含む。
ms.openlocfilehash: e38f5f2baf6bb9ade31c2778799a3ece968147f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409098"
---
# <a name="relellipticalarcto-row-geometry-section"></a><span data-ttu-id="29a32-103">[RelEllipticalArcTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="29a32-103">RelEllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="29a32-104">図形の幅と高さに対する楕円円弧の端点の x 座標と y 座標、図形の幅と高さに対する円弧上のコントロール ポイントの x 座標と *y* 座標 *、x* 軸から楕円の長軸への角度、楕円の長軸と短軸の比率を含む。 </span><span class="sxs-lookup"><span data-stu-id="29a32-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint relative to the shape's width and height,  *x*  - and  *y*  -coordinates of the control points on the arc relative to the shape's width and height, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="29a32-105">[**RelEllipticalArcTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。</span><span class="sxs-lookup"><span data-stu-id="29a32-105">A **RelEllipticalArcTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="29a32-106">ファイルを 2003 から 2010 の Visio 形式に保存すると **、RelEllipticalArcTo** 行は、エリプティカル [ArcTo](ellipticalarcto-row-geometry-section.md)行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="29a32-106">When a file is saved to the Visio 2003-2010 formats, the **RelEllipticalArcTo** row is converted to an [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="29a32-107">[**RelEllipticalArcTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="29a32-107">A **RelEllipticalArcTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="29a32-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="29a32-108">**Cell**</span></span>|<span data-ttu-id="29a32-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="29a32-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29a32-110">X</span><span class="sxs-lookup"><span data-stu-id="29a32-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="29a32-111">図形  *の*  幅を基準にした円弧上の終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="29a32-111">The  *x*  -coordinate of the ending vertex on an arc relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="29a32-112">Y</span><span class="sxs-lookup"><span data-stu-id="29a32-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="29a32-113">図形  *の高*  さを基準にした円弧上の終了頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="29a32-113">The  *y*  -coordinate of the ending vertex on an arc relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="29a32-114">A</span><span class="sxs-lookup"><span data-stu-id="29a32-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="29a32-115">図形  *の*  幅を基準にした円弧のコントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始頂点と終了頂点の約半分の位置に最適です。それ以外の場合、コントロール ポイントを通過するために極端なサイズにアークが大きくなる可能性があります。予期しない結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="29a32-115">The  *x*  -coordinate of the arc's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="29a32-116">B</span><span class="sxs-lookup"><span data-stu-id="29a32-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="29a32-117">図形  *の幅*  に対する円弧のコントロール ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="29a32-117">The  *y*  -coordinate of an arc's control point relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="29a32-118">C</span><span class="sxs-lookup"><span data-stu-id="29a32-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="29a32-119">親の x 軸に対する円弧の長軸の角度。</span><span class="sxs-lookup"><span data-stu-id="29a32-119">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="29a32-120">D</span><span class="sxs-lookup"><span data-stu-id="29a32-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="29a32-p102">円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="29a32-p102">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29a32-124">注釈</span><span class="sxs-lookup"><span data-stu-id="29a32-124">Remarks</span></span>

<span data-ttu-id="29a32-125">[**RelEllipticalArcTo**] 行の値は、図形の幅と高さを乗算した [[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)] 行の値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="29a32-125">Values in the **RelEllipticalArcTo** row are equivalent to values in an [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) row, multiplied by the width and height of the shape.</span></span> <span data-ttu-id="29a32-126">たとえば、X、Y、A、B、C、および **D** セルの値が1、1、1.5、0.5、15 deg、および 1.5 (それぞれ) の **RelEllipticalArcTo** 行を、セル式 `Width*1` `Height*1'` `Width*1.5` `Height*0.5` 、15 deg、および 1.5 (それぞれ) のセル式で、1.5 に置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="29a32-126">For example: a **RelEllipticalArcTo** row where the **X**, **Y**, **A**, **B**, **C**, and **D** cells have the values 1, 1, 1.5, 0.5, 15 deg, and 1.5 (respectively) can be replaced with an **EllipticalArcTo** row with the cell formulas  `Width*1`,  `Height*1'`,  `Width*1.5`,  `Height*0.5`, 15 deg, and 1.5 (respectively).</span></span>
  

