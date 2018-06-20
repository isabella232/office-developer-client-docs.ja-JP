---
title: '[RelQuadBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: X と y の図形の幅と高さと x の二次ベジェ曲線の端点の座標および y が含まれています-曲線の相対的な図形の幅と高さの制御点の座標です。
ms.openlocfilehash: 99796e85a857fd320598cb48993fc29bdfa4964d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806231"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="116da-103">[RelQuadBezTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="116da-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="116da-104">*X*と*y*の図形の幅と高さ、 *x*を基準にして二次ベジェ曲線の端点の座標および*y*が含まれています-曲線の相対的な図形の幅と高さの制御点の座標です。</span><span class="sxs-lookup"><span data-stu-id="116da-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="116da-105">**RelQuadBezTo**行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保持できます。</span><span class="sxs-lookup"><span data-stu-id="116da-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="116da-106">ファイル保存すると、Visio 2003 から 2010 年の書式には、 **RelQuadBezTo**行が[[nurbsto]](nurbsto-row-geometry-section.md)行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="116da-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="116da-107">**RelQuadBezTo**行には、次のセルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="116da-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="116da-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="116da-108">**Cell**</span></span>|<span data-ttu-id="116da-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="116da-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="116da-110">X</span><span class="sxs-lookup"><span data-stu-id="116da-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="116da-111">*X* -図形の幅を基準にして二次ベジェ曲線の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="116da-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="116da-112">Y</span><span class="sxs-lookup"><span data-stu-id="116da-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="116da-113">*Y* -図形の高さを基準にして二次ベジェ曲線の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="116da-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="116da-114">A</span><span class="sxs-lookup"><span data-stu-id="116da-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="116da-115">*X* -図形の幅を基準にして、曲線の制御点の座標円弧上の点。コントロール ポイントは、最初と最後の円弧の頂点の間で途中で最適に配置します。</span><span class="sxs-lookup"><span data-stu-id="116da-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="116da-116">B</span><span class="sxs-lookup"><span data-stu-id="116da-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="116da-117">*Y* -図形の高さを基準にして、曲線の制御点の座標です。</span><span class="sxs-lookup"><span data-stu-id="116da-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

