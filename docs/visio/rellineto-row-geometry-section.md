---
title: '[RelLineTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: 含まれています - x と y の図形の幅と高さを基準にして、直線の線分の終点の座標です。
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806187"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="4c172-103">[RelLineTo] 行 ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="4c172-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="4c172-104">*X*が含まれています- と*y*の図形の幅と高さを基準にして、直線の線分の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="4c172-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4c172-105">**RelLineTo**行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保持できます。</span><span class="sxs-lookup"><span data-stu-id="4c172-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="4c172-106">ファイル保存すると、Visio 2003 から 2010 年の書式には、 **RelLineTo**行が[[lineto]](lineto-row-geometry-section.md)行に変換されます。</span><span class="sxs-lookup"><span data-stu-id="4c172-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="4c172-107">[**RelLineTo**] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4c172-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="4c172-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4c172-108">**Cell**</span></span>|<span data-ttu-id="4c172-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="4c172-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c172-110">X</span><span class="sxs-lookup"><span data-stu-id="4c172-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="4c172-111">*X* -図形の幅を基準にして、直線の線分の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="4c172-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="4c172-112">Y</span><span class="sxs-lookup"><span data-stu-id="4c172-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="4c172-113">*Y* -図形の高さを基準にして、直線の線分の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="4c172-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c172-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4c172-114">Remarks</span></span>

<span data-ttu-id="4c172-115">**RelLineTo**行の値は、 [[lineto]](lineto-row-geometry-section.md)行で、幅と図形の高さを乗じた値に相当します。</span><span class="sxs-lookup"><span data-stu-id="4c172-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="4c172-116">例: **[lineto]** 行の [ **X** ] セルの値と数式があると**RelLineTo**の行の [ **X** ] セルの値が「0」、[ **Y** ] セルの値は「0.5」を置き換えることができます」*0"の幅] と [ **Y**セルは、数式"高さ*0.5」。</span><span class="sxs-lookup"><span data-stu-id="4c172-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  

