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
description: 含まれている x および y のポリラインとポリラインの数式の最後の点の座標です。
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806011"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="4a49f-103">[PolylineTo] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="4a49f-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="4a49f-104">*X*および*y*が含まれていますが、ポリラインとポリラインの数式の最後の点の座標です。</span><span class="sxs-lookup"><span data-stu-id="4a49f-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="4a49f-105">[PolylineTo] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4a49f-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="4a49f-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4a49f-106">**Cell**</span></span>|<span data-ttu-id="4a49f-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="4a49f-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a49f-108">X</span><span class="sxs-lookup"><span data-stu-id="4a49f-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="4a49f-109">*X* -ポリラインの最後の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="4a49f-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="4a49f-110">Y</span><span class="sxs-lookup"><span data-stu-id="4a49f-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="4a49f-111">*Y* -ポリラインの最後の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="4a49f-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="4a49f-112">A</span><span class="sxs-lookup"><span data-stu-id="4a49f-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="4a49f-113">ポリラインの数式です。</span><span class="sxs-lookup"><span data-stu-id="4a49f-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a49f-114">備考</span><span class="sxs-lookup"><span data-stu-id="4a49f-114">Remarks</span></span>

<span data-ttu-id="4a49f-115">ポリライン行として表される行は、[lineto] 行のシーケンスとして表される行と同じですが、ポリライン行の方が効率的です。</span><span class="sxs-lookup"><span data-stu-id="4a49f-115">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient.</span></span> <span data-ttu-id="4a49f-116">[Lineto] 行を [polylineto] 行を変更するには、図形の形状を簡単に確認することができますように。</span><span class="sxs-lookup"><span data-stu-id="4a49f-116">You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry.</span></span> <span data-ttu-id="4a49f-117">[Polylineto] 行を右クリックし、ショートカット メニューの [**行の展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a49f-117">To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="4a49f-118">行の種類を [polylineto] 行に変更するには、行を右クリックし、し、ショートカット メニューの [**行の種類の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a49f-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

