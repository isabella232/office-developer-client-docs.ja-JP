---
title: '[PolylineTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: ポリラインの最後の点とポリライン式の x 座標と y 座標を格納します。
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359830"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="4312e-103">[PolylineTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="4312e-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="4312e-104">ポリラインの最後の点とポリライン式の*x*座標と*y*座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="4312e-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="4312e-105">[PolylineTo] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4312e-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="4312e-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4312e-106">**Cell**</span></span>|<span data-ttu-id="4312e-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="4312e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4312e-108">X</span><span class="sxs-lookup"><span data-stu-id="4312e-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="4312e-109">ポリラインの最後の頂点に対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="4312e-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="4312e-110">Y</span><span class="sxs-lookup"><span data-stu-id="4312e-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="4312e-111">ポリラインの最後の頂点に対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="4312e-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="4312e-112">A</span><span class="sxs-lookup"><span data-stu-id="4312e-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="4312e-113">ポリラインの数式です。</span><span class="sxs-lookup"><span data-stu-id="4312e-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4312e-114">解説</span><span class="sxs-lookup"><span data-stu-id="4312e-114">Remarks</span></span>

<span data-ttu-id="4312e-p101">[Polyline] 行として表示される行は、一連の [LineTo] 行として表示される行と同じものです。ただし、[Polyline] 行の方が高機能です。図形の座標をより見やすくするために、[PolylineTo] 行から [LineTo] 行に変更することができます。これを行うには、[Polyline] 行を右クリックして、ショートカット メニューの **[行の拡張]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4312e-p101">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient. You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry. To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="4312e-118">行の種類を [PolylineTo] 行に変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4312e-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

