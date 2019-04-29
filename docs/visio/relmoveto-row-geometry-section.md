---
title: '[RelMoveTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: 図形の最初の頂点に対する x 座標と y 座標、またはパスを切断した後の最初の頂点に対する x 座標と y 座標を格納します。これには、図形の高さと幅を基準にします。
ms.openlocfilehash: 488945dbeeea177514770da57b5f26ac947053a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414201"
---
# <a name="relmoveto-row-geometry-section"></a><span data-ttu-id="a4d2f-103">[RelMoveTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="a4d2f-103">RelMoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="a4d2f-104">図形の最初の頂点に対する*x*座標と*y*座標、またはパスを切断した後の最初の頂点に対する*x*座標と*y*座標を格納します。これには、図形の高さと幅を基準にします。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape or the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path, relative to the height and width of the shape.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a4d2f-105">[**RelMoveTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-105">A **RelMoveTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="a4d2f-106">Visio 2003-2010 形式でファイルを保存すると、[ **relmoveto** ] 行が [ [moveto](moveto-row-geometry-section.md) ] 行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-106">When a file is saved to the Visio 2003-2010 formats, the **RelMoveTo** row is converted to a [MoveTo](moveto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="a4d2f-107">[**RelMoveTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-107">A **RelMoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="a4d2f-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a4d2f-108">**Cell**</span></span>|<span data-ttu-id="a4d2f-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4d2f-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4d2f-110">X</span><span class="sxs-lookup"><span data-stu-id="a4d2f-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a4d2f-111">[ **relmoveto** ] 行がセクションの最初の行の場合、[x] セルは図形の幅を基準にして、図形の最初の頂点に対する*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-111">If the **RelMoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape relative to the width of the shape.</span></span> <span data-ttu-id="a4d2f-112">2つの行の間に [ **relmoveto** ] 行が表示されている場合、[x] セルは、パスを切断した後の最初の頂点に対する*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-112">If the **RelMoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="a4d2f-113">Y</span><span class="sxs-lookup"><span data-stu-id="a4d2f-113">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a4d2f-114">[ **relmoveto** ] 行がセクションの最初の行の場合、[y] セルは、図形の最初の頂点に対する*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-114">If the **RelMoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="a4d2f-115">2つの行の間に [ **relmoveto** ] 行が表示されている場合、[y] セルは、パスを切断した後の最初の頂点に対する*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-115">If the **RelMoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4d2f-116">注釈</span><span class="sxs-lookup"><span data-stu-id="a4d2f-116">Remarks</span></span>

<span data-ttu-id="a4d2f-117">[**RelMoveTo**] 行の値は、図形の幅と高さを乗算した [[MoveTo](moveto-row-geometry-section.md)] 行の値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-117">Values in the **RelMoveTo** row are equivalent to values in a [MoveTo](moveto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="a4d2f-118">例: [ **x** ] セルの値が "0" で、[ **y** ] セルの値が "0.5" の場合、[ **x** ] セルの値が数式 "Width \*\*\*\* 0" で、[ \*\*\*\* \* **y** ] セルが数式である [moveto] 行に置き換えることができます。数式 "Height\*0.5."</span><span class="sxs-lookup"><span data-stu-id="a4d2f-118">For example: a **RelMoveTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" could be replaced with **MoveTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  
<span data-ttu-id="a4d2f-119">[ **relmoveto** ] 行には、[moveto] 行がセクションの最初の行である場合に、図形の最初の頂点に対する*x*座標と*y*座標が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-119">The **RelMoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the MoveTo row is the first row in the section.</span></span> <span data-ttu-id="a4d2f-120">通常、これは図形が描画されたときに最初に配置される頂点で、1-d 図形の始点には必ずしも対応していません。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-120">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="a4d2f-121">**Geometry**セクションは、[ **moveto** ] 行または [ **relmoveto** ] 行で開始する必要がありますが、図形の幅と高さに対する図形のパスの塗りつぶしのギャップを表すには、[ **relmoveto** ] 行と [ **moveto** ] 行を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-121">A **Geometry** section must begin with a **MoveTo** or a **RelMoveTo** row, but you can also use the **RelMoveTo** row and **MoveTo** row to represent a gap in the stroking of a shape's path relative to the shape's width and height.</span></span> <span data-ttu-id="a4d2f-122">ただし、パスを使用して塗りつぶされた領域の境界を定義すると、このギャップは直線セグメントとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-122">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="a4d2f-123">このような隙間を挿入するには、2つの行の間に行を挿入し、その行の種類を [**リレーションシップ**] に変更します。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-123">To insert such a gap, insert a row between two rows and change the row type to **RelMoveTo**.</span></span> <span data-ttu-id="a4d2f-124">[ **relmoveto** ] 行が2つの行の間にある場合は、図形のパスにある改行の後の行の最初の頂点に対する*x*座標と*y*座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="a4d2f-124">If the **RelMoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

