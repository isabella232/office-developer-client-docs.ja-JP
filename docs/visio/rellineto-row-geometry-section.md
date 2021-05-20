---
title: '[RelLineTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: 図形の幅と高さを基準にした直線セグメントの終了頂点の x 座標と y 座標を含む。
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437162"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="44577-103">[RelLineTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="44577-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="44577-104">図形の  *幅*  と高さを基準にした直線セグメントの終了頂点の x 座標と  *y*  座標を含む。</span><span class="sxs-lookup"><span data-stu-id="44577-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="44577-105">[**RelLineTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。</span><span class="sxs-lookup"><span data-stu-id="44577-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="44577-106">ファイルを 2003- 2010 形式Visio保存すると **、RelLineTo** 行は [LineTo 行に変換](lineto-row-geometry-section.md)されます。</span><span class="sxs-lookup"><span data-stu-id="44577-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="44577-107">[**RelLineTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="44577-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="44577-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="44577-108">**Cell**</span></span>|<span data-ttu-id="44577-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="44577-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44577-110">X</span><span class="sxs-lookup"><span data-stu-id="44577-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="44577-111">図形  *の*  幅を基準にした直線セグメントの終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="44577-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="44577-112">Y</span><span class="sxs-lookup"><span data-stu-id="44577-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="44577-113">図形  *の高*  さを基準にした直線セグメントの終了頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="44577-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44577-114">注釈</span><span class="sxs-lookup"><span data-stu-id="44577-114">Remarks</span></span>

<span data-ttu-id="44577-115">[**RelLineTo**] 行の値は、図形の幅と高さを乗算した [[LineTo](lineto-row-geometry-section.md)] 行の値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="44577-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="44577-116">たとえば **、X** セルの値が "0" で **、Y** セルの値が "0.5" の **RelLineTo** 行は **、X** セルの値が数式 "Width *0" で **、Y*** セルが数式 "Height 0.5" である **LineTo** 行に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="44577-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width *0" and the **Y** cell is the formula "Height* 0.5."</span></span> 
  

