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
description: 図形の最初の頂点に対する x 座標と y 座標を格納します。または、パスを切断した後の最初の頂点に対する x 座標と y 座標を表します。
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429699"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="005ae-103">[MoveTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="005ae-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="005ae-104">図形の最初の頂点に対する*x*座標と*y*座標を格納します。または、パスを切断した後の最初の頂点に対する*x*座標と*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="005ae-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="005ae-105">[**MoveTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="005ae-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="005ae-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="005ae-106">**Cell**</span></span>|<span data-ttu-id="005ae-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="005ae-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="005ae-108">X</span><span class="sxs-lookup"><span data-stu-id="005ae-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="005ae-109">[ **MoveTo** ] 行がセクションの最初の行の場合、[x] セルは、図形の最初の頂点に対する*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="005ae-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="005ae-110">[ **MoveTo** ] 行が2つの行の間に表示される場合、[x] セルは、パスを切断した後の最初の頂点に対する*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="005ae-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="005ae-111">Y</span><span class="sxs-lookup"><span data-stu-id="005ae-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="005ae-112">[ **MoveTo** ] 行がセクションの最初の行の場合、[y] セルは、図形の最初の頂点に対する*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="005ae-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="005ae-113">[ **MoveTo** ] 行が2つの行の間に表示される場合、[y] セルは、パスを切断した後の最初の頂点に対する*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="005ae-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="005ae-114">注釈</span><span class="sxs-lookup"><span data-stu-id="005ae-114">Remarks</span></span>

<span data-ttu-id="005ae-115">[ **moveto** ] 行には、[ **moveto** ] 行がセクションの最初の行である場合に、図形の最初の頂点に対する*x*座標と*y*座標が含まれます。</span><span class="sxs-lookup"><span data-stu-id="005ae-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="005ae-116">通常、これは図形が描画されたときに最初に配置される頂点で、1-d 図形の始点には必ずしも対応していません。</span><span class="sxs-lookup"><span data-stu-id="005ae-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="005ae-117">[geometry] セクションは、[ **relmoveto** ] 行または [ **moveto** ] 行で開始する必要がありますが、図形のパスの描画のギャップを表すのには、 **moveto**と**relmoveto**の行を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="005ae-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="005ae-118">ただし、パスを使用して塗りつぶされた領域の境界を定義すると、このギャップは直線セグメントとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="005ae-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="005ae-119">このような隙間を挿入するには、2つの行の間に行を挿入し、その行の種類を [ **MoveTo**] に変更します。</span><span class="sxs-lookup"><span data-stu-id="005ae-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="005ae-120">[ **MoveTo** ] 行が2つの行の間にある場合は、図形のパスにある改行の後の最初の頂点に対する*x*座標と*y*座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="005ae-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

