---
title: '[MoveTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: 図形の最初の頂点の x 座標と y 座標、またはパスのブレーク後の最初の頂点の x 座標と y 座標を表します。
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429699"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="a2d52-103">[MoveTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="a2d52-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="a2d52-104">図形の最初の頂点の  *x*  座標と  *y*  座標、またはパスのブレーク後の最初の頂点の  *x*  座標と  *y*  座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a2d52-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="a2d52-105">[**MoveTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a2d52-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="a2d52-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a2d52-106">**Cell**</span></span>|<span data-ttu-id="a2d52-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="a2d52-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2d52-108">X</span><span class="sxs-lookup"><span data-stu-id="a2d52-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a2d52-109">**MoveTo 行** がセクションの最初の行である場合、X セルは図形の最初の頂点の *x* 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a2d52-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="a2d52-110">**MoveTo 行が 2** 行の間に表示される場合、X セルはパスのブレーク後の最初の頂点の *x* 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a2d52-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="a2d52-111">Y</span><span class="sxs-lookup"><span data-stu-id="a2d52-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a2d52-112">**MoveTo 行** がセクションの最初の行である場合、Y セルは図形の最初の頂点の *y* 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a2d52-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="a2d52-113">**MoveTo 行が 2** 行の間に表示される場合、Y セルはパスのブレーク後の最初の頂点の *y* 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a2d52-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2d52-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a2d52-114">Remarks</span></span>

<span data-ttu-id="a2d52-115">**MoveTo 行** には *、MoveTo* 行がセクションの最初の行である場合、図形の最初の頂点の x 座標と *y* 座標が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a2d52-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="a2d52-116">通常、これは図形が描画された時点で最初に配置される頂点であり、必ずしも 1-D 図形の開始点に対応するとは限りません。</span><span class="sxs-lookup"><span data-stu-id="a2d52-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="a2d52-117">ジオメトリ セクションは **RelMoveTo** 行または **MoveTo** 行で始まる必要がありますが **、MoveTo** 行と **RelMoveTo** 行を使用して、図形のパスのストロークのギャップを表することもできます。</span><span class="sxs-lookup"><span data-stu-id="a2d52-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="a2d52-118">ただし、塗りつぶされた領域の境界を定義するためにパスを使用すると、このギャップは直線セグメントとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="a2d52-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="a2d52-119">このようなギャップを挿入するには、2 つの行の間に行を挿入し、行の種類を **MoveTo に変更します**。</span><span class="sxs-lookup"><span data-stu-id="a2d52-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="a2d52-120">**MoveTo 行が 2** 行の間にある場合、図形のパスでブレークした後の線の最初の頂点の *x* 座標と *y* 座標が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a2d52-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

