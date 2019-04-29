---
title: '[RelLineTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: 図形の幅と高さに相対する直線セグメントの最後の頂点に対する x 座標と y 座標を格納します。
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437162"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="d7ece-103">[RelLineTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="d7ece-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="d7ece-104">図形の幅と高さに相対する直線セグメントの最後の頂点に対する*x*座標と*y*座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="d7ece-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d7ece-105">[**RelLineTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。</span><span class="sxs-lookup"><span data-stu-id="d7ece-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="d7ece-106">ファイルを Visio 2003-2010 形式に保存すると、[ **rellineto** ] 行は[lineto](lineto-row-geometry-section.md)行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="d7ece-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="d7ece-107">[**RelLineTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d7ece-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="d7ece-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d7ece-108">**Cell**</span></span>|<span data-ttu-id="d7ece-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="d7ece-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7ece-110">X</span><span class="sxs-lookup"><span data-stu-id="d7ece-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="d7ece-111">図形の幅を基準にして、直線セグメントの最後の頂点に対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="d7ece-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="d7ece-112">Y</span><span class="sxs-lookup"><span data-stu-id="d7ece-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="d7ece-113">図形の高さを基準にして、直線セグメントの最後の頂点に対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="d7ece-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7ece-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d7ece-114">Remarks</span></span>

<span data-ttu-id="d7ece-115">[**RelLineTo**] 行の値は、図形の幅と高さを乗算した [[LineTo](lineto-row-geometry-section.md)] 行の値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="d7ece-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="d7ece-116">例: [ **x** ] セルの値が "0" で、[ **y** ] セルの値が "0.5" である [ **lineto** ] 行に置き換えることができるのは、[ **x** ] セルの値が数式 "Width \*\*\*\* *0"、[ **y** ] セルが、数式 "Height*0.5."</span><span class="sxs-lookup"><span data-stu-id="d7ece-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  

