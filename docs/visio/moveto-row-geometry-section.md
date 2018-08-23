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
description: X および y が含まれています、図形の最初の頂点の座標または x を表すと y のパス内の改行の後の最初の頂点の座標です。
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805909"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="3395e-103">[MoveTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="3395e-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="3395e-104">*X*および*y*が含まれています、図形の最初の頂点の座標または*x*を表すと*y*のパス内の改行の後の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="3395e-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="3395e-105">[**MoveTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3395e-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="3395e-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3395e-106">**Cell**</span></span>|<span data-ttu-id="3395e-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="3395e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3395e-108">X</span><span class="sxs-lookup"><span data-stu-id="3395e-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="3395e-109">**[Moveto]** 行がセクションの最初の行の場合は、[X] セルは*x*を表しますが、図形の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="3395e-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="3395e-110">[X] セルが*x*を表す 2 つの行の間、 **[moveto]** 行が表示されている場合のパスを切断した後の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="3395e-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="3395e-111">Y</span><span class="sxs-lookup"><span data-stu-id="3395e-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="3395e-112">**[Moveto]** 行がセクションの最初の行の場合は、[Y] セルは*y*を表す-図形の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="3395e-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="3395e-113">[Y] セルが*y*を表す 2 つの行の間、 **[moveto]** 行が表示されている場合のパスを切断した後の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="3395e-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3395e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3395e-114">Remarks</span></span>

<span data-ttu-id="3395e-115">**[Moveto]** 行には、 *x*および*y*が含まれています- **[moveto]** 行がセクションの最初の行である場合の図形の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="3395e-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="3395e-116">通常これは図形が描画されて、および 1-d 図形の始点に必ずしも対応していないときに配置する最初の頂点です。</span><span class="sxs-lookup"><span data-stu-id="3395e-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="3395e-117">[Geometry] セクションは、 **RelMoveTo**または **[moveto]** 行では、いずれかで始まる必要がありますが、図形のパスの描画にギャップを表すため、 **[moveto]** 行と**RelMoveTo**行を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="3395e-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="3395e-118">ただし、塗りつぶされた領域の境界を定義するのには、パスを使用する場合は、このギャップが直線セグメントとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="3395e-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="3395e-119">このようなギャップを挿入するには、2 つの行の間で行を挿入し、行の種類を **[moveto]** に変更します。</span><span class="sxs-lookup"><span data-stu-id="3395e-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="3395e-120">**[Moveto]** 行が 2 行の間にある場合は、含まれている、 *x*および*y*の図形のパスを切断した後の行の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="3395e-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

