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
description: 含まれています x および y-楕円の円弧の端点、x および y の座標-、円弧のコントロール ポイントの座標が x の角度の軸には、楕円の長軸、および楕円の長軸と短軸の軸との間の比率。
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805302"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="ac891-103">[EllipticalArcTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="ac891-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="ac891-104">*X*および*y* 、 *x*の楕円の円弧の終点の座標が含まれていますと*y*の、円弧のコントロール ポイントの座標が*x*の角度の軸には、楕円の長軸、および楕円のメジャーと mino の比率。r 軸です。</span><span class="sxs-lookup"><span data-stu-id="ac891-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="ac891-105">[EllipticalArcTo] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ac891-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="ac891-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ac891-106">**Cell**</span></span>|<span data-ttu-id="ac891-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="ac891-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac891-108">X</span><span class="sxs-lookup"><span data-stu-id="ac891-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="ac891-109">*X*の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="ac891-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="ac891-110">Y</span><span class="sxs-lookup"><span data-stu-id="ac891-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="ac891-111">*Y*の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="ac891-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="ac891-112">A</span><span class="sxs-lookup"><span data-stu-id="ac891-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="ac891-113">*X*の円弧のコントロール ポイントの座標円弧上の点。コントロール ポイントは、最初と最後の円弧の頂点の間で途中で最適に配置します。それ以外の場合、円弧は、予期しない結果で、コントロール ポイントを通過するために極端になることがあります。</span><span class="sxs-lookup"><span data-stu-id="ac891-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="ac891-114">B</span><span class="sxs-lookup"><span data-stu-id="ac891-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="ac891-115">*Y*の円弧のコントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="ac891-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="ac891-116">C</span><span class="sxs-lookup"><span data-stu-id="ac891-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="ac891-117">*X*を基準にして、円弧の長軸の角度を親の軸です。</span><span class="sxs-lookup"><span data-stu-id="ac891-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="ac891-118">D</span><span class="sxs-lookup"><span data-stu-id="ac891-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="ac891-p101">円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ac891-p101">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

