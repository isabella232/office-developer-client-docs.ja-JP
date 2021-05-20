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
description: 円弧の x 座標と y 座標と弓を格納します。
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430043"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="ac8c3-103">[ArcTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="ac8c3-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="ac8c3-104">円弧の  *x*  座標と  *y*  座標と弓を格納します。</span><span class="sxs-lookup"><span data-stu-id="ac8c3-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="ac8c3-105">[ArcTo] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ac8c3-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="ac8c3-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ac8c3-106">**Cell**</span></span>|<span data-ttu-id="ac8c3-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="ac8c3-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac8c3-108">X</span><span class="sxs-lookup"><span data-stu-id="ac8c3-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="ac8c3-109">円弧  *の*  終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="ac8c3-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="ac8c3-110">Y</span><span class="sxs-lookup"><span data-stu-id="ac8c3-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="ac8c3-111">円弧  *の終了*  頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="ac8c3-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="ac8c3-112">A</span><span class="sxs-lookup"><span data-stu-id="ac8c3-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="ac8c3-113">円弧の中点から弦の中点までの距離です。</span><span class="sxs-lookup"><span data-stu-id="ac8c3-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac8c3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ac8c3-114">Remarks</span></span>

<span data-ttu-id="ac8c3-p101">Visio で描画する弧は、真円に基づいている場合でも、楕円の弧になります。既定では、描画された弧は [シェイプシート] ウィンドウの [EllipticalArcTo] 行で表されます。[ArcTo] 行を [シェイプシート] ウィンドウに表示するには、弧を描画してから、行の種類を [EllipticalArcTo] から [ArcTo] に変更します。この結果、楕円の弧が真円の弧に変換されます。</span><span class="sxs-lookup"><span data-stu-id="ac8c3-p101">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle. By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window. To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="ac8c3-118">行の種類を変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac8c3-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

