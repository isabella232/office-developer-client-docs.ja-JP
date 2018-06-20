---
title: '[RelMoveTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: X と y の最初の頂点、図形の x 座標の y が含まれていますが、図形の幅と高さを基準にして、パス内の改行の後の最初の頂点の座標です。
ms.openlocfilehash: 77b3e731bfd1f35abe34ffbf3155b57133e56412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806198"
---
# <a name="relmoveto-row-geometry-section"></a><span data-ttu-id="eeec2-103">[RelMoveTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="eeec2-103">RelMoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="eeec2-104">*X*と*y*の最初の頂点、図形の*x*座標を*y*が含まれていますが、図形の幅と高さを基準にして、パス内の改行の後の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="eeec2-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape or the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path, relative to the height and width of the shape.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eeec2-105">**RelMoveTo**行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保持できます。</span><span class="sxs-lookup"><span data-stu-id="eeec2-105">A **RelMoveTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="eeec2-106">Visio 2003 から 2010 年の形式にファイルを保存すると、 **RelMoveTo**の行は[[moveto]](moveto-row-geometry-section.md)行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="eeec2-106">When a file is saved to the Visio 2003-2010 formats, the **RelMoveTo** row is converted to a [MoveTo](moveto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="eeec2-107">**RelMoveTo**行には、次のセルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="eeec2-107">A **RelMoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="eeec2-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="eeec2-108">**Cell**</span></span>|<span data-ttu-id="eeec2-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="eeec2-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eeec2-110">X</span><span class="sxs-lookup"><span data-stu-id="eeec2-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="eeec2-111">**RelMoveTo**行がセクションの最初の行の場合は、[X] セルは*x*を表しますが、図形の幅を基準に図形の最初の頂点の座標。</span><span class="sxs-lookup"><span data-stu-id="eeec2-111">If the **RelMoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape relative to the width of the shape.</span></span> <span data-ttu-id="eeec2-112">[X] セルが*x*を表す 2 つの行の間に**RelMoveTo**行が表示されている場合のパスを切断した後の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="eeec2-112">If the **RelMoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="eeec2-113">Y</span><span class="sxs-lookup"><span data-stu-id="eeec2-113">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="eeec2-114">[Y] セルが*y*を表す**RelMoveTo**の行がセクションの最初の行の場合は、最初の図形の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="eeec2-114">If the **RelMoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="eeec2-115">[Y] セルが*y*を表す 2 つの行の間に**RelMoveTo**行が表示されている場合のパスを切断した後の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="eeec2-115">If the **RelMoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eeec2-116">備考</span><span class="sxs-lookup"><span data-stu-id="eeec2-116">Remarks</span></span>

<span data-ttu-id="eeec2-117">**RelMoveTo**行の値は、 [[moveto]](moveto-row-geometry-section.md)行で、幅と図形の高さを乗じた値に相当します。</span><span class="sxs-lookup"><span data-stu-id="eeec2-117">Values in the **RelMoveTo** row are equivalent to values in a [MoveTo](moveto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="eeec2-118">例: [ **X** ] セルの値が数式にある **[moveto]** 行で [ **X** ] セルの値が「0」は、[ **Y** ] セルの値は「0.5」は、 **RelMoveTo**行を置き換えることができます」*0"の幅] と [ **Y** ] セルは、数式"高さ*0.5」。</span><span class="sxs-lookup"><span data-stu-id="eeec2-118">For example: a **RelMoveTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" could be replaced with **MoveTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  
<span data-ttu-id="eeec2-119">**RelMoveTo**行には、 *x*および*y*が含まれています-[moveto] 行がセクションの最初の行である場合の図形の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="eeec2-119">The **RelMoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the MoveTo row is the first row in the section.</span></span> <span data-ttu-id="eeec2-120">通常これは図形が描画されて、および 1-d 図形の始点に必ずしも対応していないときに配置する最初の頂点です。</span><span class="sxs-lookup"><span data-stu-id="eeec2-120">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="eeec2-121">**[Geometry** ] セクションを **[moveto]** または**RelMoveTo**の行を開始する必要がありますが、図形の幅と高さを基準にして図形のパスの描画にギャップを表すため、 **RelMoveTo**の行と **[moveto]** 行を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="eeec2-121">A **Geometry** section must begin with a **MoveTo** or a **RelMoveTo** row, but you can also use the **RelMoveTo** row and **MoveTo** row to represent a gap in the stroking of a shape's path relative to the shape's width and height.</span></span> <span data-ttu-id="eeec2-122">ただし、塗りつぶされた領域の境界を定義するのには、パスを使用する場合は、このギャップが直線セグメントとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="eeec2-122">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="eeec2-123">このようなギャップを挿入するには、2 つの行の間で行を挿入し、行の種類を**RelMoveTo**に変更します。</span><span class="sxs-lookup"><span data-stu-id="eeec2-123">To insert such a gap, insert a row between two rows and change the row type to **RelMoveTo**.</span></span> <span data-ttu-id="eeec2-124">**RelMoveTo**行が 2 行の間にある場合は、含まれている、 *x*および*y*の図形のパスを切断した後の行の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="eeec2-124">If the **RelMoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

