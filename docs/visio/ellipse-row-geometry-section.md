---
title: '[Ellipse] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: 楕円の中心点と楕円上の2つの点に対する x 座標と y 座標を格納します。
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345683"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="579f1-103">[Ellipse] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="579f1-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="579f1-104">楕円の中心点と楕円上の2つの点に対する*x*座標と*y*座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="579f1-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="579f1-105">[Ellipse] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="579f1-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="579f1-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="579f1-106">**Cell**</span></span>|<span data-ttu-id="579f1-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="579f1-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="579f1-108">X</span><span class="sxs-lookup"><span data-stu-id="579f1-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="579f1-109">中心点の*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="579f1-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="579f1-110">Y</span><span class="sxs-lookup"><span data-stu-id="579f1-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="579f1-111">中心点の*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="579f1-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="579f1-112">A</span><span class="sxs-lookup"><span data-stu-id="579f1-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="579f1-113">楕円上の1点の x 座標です。対応する*y*座標は [B セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="579f1-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="579f1-114">B</span><span class="sxs-lookup"><span data-stu-id="579f1-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="579f1-115">楕円上の1点の*y*座標です。対応する x 座標は、A セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="579f1-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="579f1-116">C</span><span class="sxs-lookup"><span data-stu-id="579f1-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="579f1-117">楕円上の別の点の*x*座標です。対応する*y*座標は [D セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="579f1-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="579f1-118">D</span><span class="sxs-lookup"><span data-stu-id="579f1-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="579f1-119">楕円上の別の点の*y*座標です。対応する*y*座標は [C セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="579f1-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="579f1-120">解説</span><span class="sxs-lookup"><span data-stu-id="579f1-120">Remarks</span></span>

<span data-ttu-id="579f1-121">[Ellipse] 行または [InfiniteLine] 行を含む [Geometry] セクションには、他の行を入れることができません。</span><span class="sxs-lookup"><span data-stu-id="579f1-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

