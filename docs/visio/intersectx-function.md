---
title: INTERSECTX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: 2本の線が交わる点の x 座標 (ローカル座標系) を返します。
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335309"
---
# <a name="intersectx-function"></a><span data-ttu-id="6c1f1-103">INTERSECTX 関数</span><span class="sxs-lookup"><span data-stu-id="6c1f1-103">INTERSECTX Function</span></span>

<span data-ttu-id="6c1f1-104">2本の線が交わる点の*x*座標 (ローカル座標系) を返します。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6c1f1-105">構文</span><span class="sxs-lookup"><span data-stu-id="6c1f1-105">Syntax</span></span>

<span data-ttu-id="6c1f1-106">INTERSECTX (\* \* *x1* \* *、* \* *y1* \* *、* \* *angle1* \* *、* \* *x2* \* *、* \* *y2* \* *、* \* *angle2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6c1f1-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6c1f1-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c1f1-107">Parameters</span></span>

|<span data-ttu-id="6c1f1-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-108">**Name**</span></span>|<span data-ttu-id="6c1f1-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-109">**Required/Optional**</span></span>|<span data-ttu-id="6c1f1-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-110">**Data Type**</span></span>|<span data-ttu-id="6c1f1-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6c1f1-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="6c1f1-112">_x1_</span></span> <br/> |<span data-ttu-id="6c1f1-113">必須</span><span class="sxs-lookup"><span data-stu-id="6c1f1-113">Required</span></span>  <br/> |<span data-ttu-id="6c1f1-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-114">**Number**</span></span> <br/> |<span data-ttu-id="6c1f1-115">最初の線にある点の_x_座標です。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="6c1f1-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="6c1f1-116">_y1_</span></span> <br/> |<span data-ttu-id="6c1f1-117">必須</span><span class="sxs-lookup"><span data-stu-id="6c1f1-117">Required</span></span>  <br/> |<span data-ttu-id="6c1f1-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-118">**Number**</span></span> <br/> |<span data-ttu-id="6c1f1-119">最初の線にある点の_y_座標です。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="6c1f1-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="6c1f1-120">_angle1_</span></span> <br/> |<span data-ttu-id="6c1f1-121">必須</span><span class="sxs-lookup"><span data-stu-id="6c1f1-121">Required</span></span>  <br/> |<span data-ttu-id="6c1f1-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-122">**Number**</span></span> <br/> | <span data-ttu-id="6c1f1-123">1 本目の線の [Angle] セルにある値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="6c1f1-124">_x_</span><span class="sxs-lookup"><span data-stu-id="6c1f1-124">_x2_</span></span> <br/> |<span data-ttu-id="6c1f1-125">必須</span><span class="sxs-lookup"><span data-stu-id="6c1f1-125">Required</span></span>  <br/> |<span data-ttu-id="6c1f1-126">**数値**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-126">**Number**</span></span> <br/> |<span data-ttu-id="6c1f1-127">2番目の線にある点の_x_座標です。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="6c1f1-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="6c1f1-128">_y2_</span></span> <br/> |<span data-ttu-id="6c1f1-129">必須</span><span class="sxs-lookup"><span data-stu-id="6c1f1-129">Required</span></span>  <br/> |<span data-ttu-id="6c1f1-130">**数値**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-130">**Number**</span></span> <br/> |<span data-ttu-id="6c1f1-131">2番目の線にある点の_y_座標です。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="6c1f1-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="6c1f1-132">_angle2_</span></span> <br/> |<span data-ttu-id="6c1f1-133">必須</span><span class="sxs-lookup"><span data-stu-id="6c1f1-133">Required</span></span>  <br/> |<span data-ttu-id="6c1f1-134">**数値**</span><span class="sxs-lookup"><span data-stu-id="6c1f1-134">**Number**</span></span> <br/> |<span data-ttu-id="6c1f1-135">2 本目の線の [Angle] セルにある値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6c1f1-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="6c1f1-136">Return value</span></span>

<span data-ttu-id="6c1f1-137">番号</span><span class="sxs-lookup"><span data-stu-id="6c1f1-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6c1f1-138">解説</span><span class="sxs-lookup"><span data-stu-id="6c1f1-138">Remarks</span></span>

<span data-ttu-id="6c1f1-139">各線は点 (*x,y*) と角度によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="6c1f1-140">Microsoft Visio で、この関数は、回転したガイドに接着されている図形の [PinX] セルで使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="6c1f1-141">2 本の線が交差しない場合、この関数はゼロで除算したことを示すエラー (#DIV/0!) を返します。Visio ではこのエラーは無視され、最後に設定された点の座標値を復元します。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6c1f1-142">例</span><span class="sxs-lookup"><span data-stu-id="6c1f1-142">Example</span></span>

<span data-ttu-id="6c1f1-143">INTERSECTX (vertguide!PinX、vertguide!PinY、vertguide!Angle、HorzGuide!PinX、HorzGuide!PinY、HorzGuide!直交</span><span class="sxs-lookup"><span data-stu-id="6c1f1-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="6c1f1-144">vertguide と HorzGuide の交差点の*x*座標をページ単位で返します。</span><span class="sxs-lookup"><span data-stu-id="6c1f1-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

