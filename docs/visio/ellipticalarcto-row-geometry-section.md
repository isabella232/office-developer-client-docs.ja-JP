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
description: 楕円円弧の端点の x 座標と y 座標、円弧上のコントロール ポイントの x 座標と y 座標、x 軸から楕円の長軸への角度、楕円の長軸と短軸の比率を含む。
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421404"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="bca0a-103">[EllipticalArcTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="bca0a-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="bca0a-104">楕円円弧の端点の x 座標と y 座標、円弧上のコントロール ポイントの x 座標と *y* 座標 *、x* 軸から楕円の長軸への角度、楕円の長軸と短軸の比率を含む。 </span><span class="sxs-lookup"><span data-stu-id="bca0a-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="bca0a-105">[EllipticalArcTo] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bca0a-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="bca0a-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="bca0a-106">**Cell**</span></span>|<span data-ttu-id="bca0a-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="bca0a-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bca0a-108">X</span><span class="sxs-lookup"><span data-stu-id="bca0a-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="bca0a-109">円弧  *上*  の終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="bca0a-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="bca0a-110">Y</span><span class="sxs-lookup"><span data-stu-id="bca0a-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="bca0a-111">円弧  *上の*  終了頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="bca0a-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="bca0a-112">A</span><span class="sxs-lookup"><span data-stu-id="bca0a-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="bca0a-113">円弧  *の*  コントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始頂点と終了頂点の約半分の位置に最適です。それ以外の場合、コントロール ポイントを通過するために極端なサイズにアークが大きくなる可能性があります。予期しない結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="bca0a-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="bca0a-114">B</span><span class="sxs-lookup"><span data-stu-id="bca0a-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="bca0a-115">円弧  *のコントロール*  ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="bca0a-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="bca0a-116">C</span><span class="sxs-lookup"><span data-stu-id="bca0a-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="bca0a-117">親の x 軸に対する円弧の長軸の角度。</span><span class="sxs-lookup"><span data-stu-id="bca0a-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="bca0a-118">D</span><span class="sxs-lookup"><span data-stu-id="bca0a-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="bca0a-p101">円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bca0a-p101">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

