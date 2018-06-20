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
description: X および y が含まれていますが、楕円の中心点および楕円上の 2 つの点の座標です。
ms.openlocfilehash: 0a2acb0efa20f67d04581f827edbfc4fb4a2d6b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805300"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="91c3b-103">[Ellipse] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="91c3b-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="91c3b-104">*X*および*y*が含まれていますが、楕円の中心点および楕円上の 2 つの点の座標です。</span><span class="sxs-lookup"><span data-stu-id="91c3b-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="91c3b-105">[Ellipse] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="91c3b-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="91c3b-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="91c3b-106">**Cell**</span></span>|<span data-ttu-id="91c3b-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="91c3b-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91c3b-108">X</span><span class="sxs-lookup"><span data-stu-id="91c3b-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="91c3b-109">*X*の中心点の座標です。</span><span class="sxs-lookup"><span data-stu-id="91c3b-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="91c3b-110">Y</span><span class="sxs-lookup"><span data-stu-id="91c3b-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="91c3b-111">*Y*の中心点の座標です。</span><span class="sxs-lookup"><span data-stu-id="91c3b-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="91c3b-112">A</span><span class="sxs-lookup"><span data-stu-id="91c3b-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="91c3b-113">楕円上の 1 つの点の x 座標対応する*y*の座標は、[B] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="91c3b-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="91c3b-114">B</span><span class="sxs-lookup"><span data-stu-id="91c3b-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="91c3b-115">*Y* -楕円上の 1 つの点の座標対応する x 座標は [A] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="91c3b-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="91c3b-116">C</span><span class="sxs-lookup"><span data-stu-id="91c3b-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="91c3b-117">*X* -楕円上の別の点の座標対応する*y*の座標は [D] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="91c3b-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="91c3b-118">D</span><span class="sxs-lookup"><span data-stu-id="91c3b-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="91c3b-119">*Y* -楕円上の別の点の座標対応する*y*の座標は、[C] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="91c3b-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91c3b-120">備考</span><span class="sxs-lookup"><span data-stu-id="91c3b-120">Remarks</span></span>

<span data-ttu-id="91c3b-121">[Ellipse] 行または [InfiniteLine] 行を含む [Geometry] セクションには、他の行を入れることができません。</span><span class="sxs-lookup"><span data-stu-id="91c3b-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

