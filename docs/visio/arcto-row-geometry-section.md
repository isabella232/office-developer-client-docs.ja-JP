---
title: '[ArcTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: X と y の座標、円弧の弓。
ms.openlocfilehash: 77ed0dcaee7ddefa8771d3e890776d4adfcc3b40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804782"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="4d750-103">[ArcTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="4d750-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="4d750-104">*X*と*y*の座標、円弧の弓。</span><span class="sxs-lookup"><span data-stu-id="4d750-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="4d750-105">[ArcTo] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4d750-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="4d750-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4d750-106">**Cell**</span></span>|<span data-ttu-id="4d750-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="4d750-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d750-108">X</span><span class="sxs-lookup"><span data-stu-id="4d750-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="4d750-109">*X*の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="4d750-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="4d750-110">Y</span><span class="sxs-lookup"><span data-stu-id="4d750-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="4d750-111">*Y*の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="4d750-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="4d750-112">A</span><span class="sxs-lookup"><span data-stu-id="4d750-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="4d750-113">円弧の中点から弦の中点までの距離です。</span><span class="sxs-lookup"><span data-stu-id="4d750-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d750-114">備考</span><span class="sxs-lookup"><span data-stu-id="4d750-114">Remarks</span></span>

<span data-ttu-id="4d750-p101">Visio で描画する弧は、真円に基づいている場合でも、楕円の弧になります。既定では、描画された弧は [シェイプシート] ウィンドウの [EllipticalArcTo] 行で表されます。[ArcTo] 行を [シェイプシート] ウィンドウに表示するには、弧を描画してから、行の種類を [EllipticalArcTo] から [ArcTo] に変更します。この結果、楕円の弧が真円の弧に変換されます。</span><span class="sxs-lookup"><span data-stu-id="4d750-p101">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle. By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window. To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="4d750-118">行の種類を変更するに、行を右クリックし、し、ショートカット メニューの [**行の種類の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d750-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

