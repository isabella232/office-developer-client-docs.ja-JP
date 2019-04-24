---
title: '[EllipticalArcTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: 楕円の弧の端点に対する x 座標と y 座標、円弧のコントロールポイントの x 座標と y 座標、x 軸から楕円の長軸までの角度、および楕円の長軸と短軸との比率を格納します。
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345676"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="c425b-103">[EllipticalArcTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="c425b-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="c425b-104">楕円の弧の端点に対する*x*座標と*y*座標、円弧のコントロールポイントの*x*座標と*y*座標、 *x*軸から楕円の長軸までの角度、および楕円の長軸と mino の比率を格納します。r 軸</span><span class="sxs-lookup"><span data-stu-id="c425b-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="c425b-105">[EllipticalArcTo] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c425b-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="c425b-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="c425b-106">**Cell**</span></span>|<span data-ttu-id="c425b-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="c425b-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c425b-108">X</span><span class="sxs-lookup"><span data-stu-id="c425b-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="c425b-109">円弧の最後の頂点に対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="c425b-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="c425b-110">Y</span><span class="sxs-lookup"><span data-stu-id="c425b-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="c425b-111">円弧の最後の頂点に対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="c425b-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="c425b-112">A</span><span class="sxs-lookup"><span data-stu-id="c425b-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="c425b-113">円弧のコントロールポイントの*x*座標です。弧の点を指定します。コントロールポイントは、円弧の始点と終点の間の中間点を中心に配置されます。それ以外の場合、円弧はコントロールポイントを通過するために極端なサイズまで拡大することがあり、予期しない結果が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="c425b-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="c425b-114">B</span><span class="sxs-lookup"><span data-stu-id="c425b-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="c425b-115">円弧のコントロールポイントの*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="c425b-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="c425b-116">C</span><span class="sxs-lookup"><span data-stu-id="c425b-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="c425b-117">親の*x*軸を基準にした円弧の主軸の角度。</span><span class="sxs-lookup"><span data-stu-id="c425b-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="c425b-118">D</span><span class="sxs-lookup"><span data-stu-id="c425b-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="c425b-p101">円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c425b-p101">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

