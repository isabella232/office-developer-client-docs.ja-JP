---
title: INTERSECTY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Y を返しますが、ローカル座標系で) の 2 本の線が交差する点の座標です。
ms.openlocfilehash: c3c0e9afef317ed4c647f1d236c4c3a29c6cdaa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805591"
---
# <a name="intersecty-function"></a><span data-ttu-id="8d208-103">INTERSECTY 関数</span><span class="sxs-lookup"><span data-stu-id="8d208-103">INTERSECTY Function</span></span>

<span data-ttu-id="8d208-104">*Y*が返されますが、ローカル座標系で) の 2 本の線が交差する点の座標です。</span><span class="sxs-lookup"><span data-stu-id="8d208-104">Returns the  *y*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d208-105">構文</span><span class="sxs-lookup"><span data-stu-id="8d208-105">Syntax</span></span>

<span data-ttu-id="8d208-106">INTERSECTX (* * *x1* * *、* * *y1* * *、* * *angle1* * *、* * *x2* * *、* * *y2* * *、* * *angle2* * *)</span><span class="sxs-lookup"><span data-stu-id="8d208-106">INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d208-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8d208-107">Parameters</span></span>

|<span data-ttu-id="8d208-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="8d208-108">**Name**</span></span>|<span data-ttu-id="8d208-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="8d208-109">**Required/Optional**</span></span>|<span data-ttu-id="8d208-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="8d208-110">**Data Type**</span></span>|<span data-ttu-id="8d208-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="8d208-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d208-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="8d208-112">_x1_</span></span> <br/> |<span data-ttu-id="8d208-113">必須</span><span class="sxs-lookup"><span data-stu-id="8d208-113">Required</span></span>  <br/> |<span data-ttu-id="8d208-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="8d208-114">**Number**</span></span> <br/> |<span data-ttu-id="8d208-115">_X_の最初の行の上の点の座標です。</span><span class="sxs-lookup"><span data-stu-id="8d208-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="8d208-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="8d208-116">_y1_</span></span> <br/> |<span data-ttu-id="8d208-117">必須</span><span class="sxs-lookup"><span data-stu-id="8d208-117">Required</span></span>  <br/> |<span data-ttu-id="8d208-118">**番号**</span><span class="sxs-lookup"><span data-stu-id="8d208-118">**Number**</span></span> <br/> |<span data-ttu-id="8d208-119">_Y_-最初の行の上の点の座標です。</span><span class="sxs-lookup"><span data-stu-id="8d208-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="8d208-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="8d208-120">_angle1_</span></span> <br/> |<span data-ttu-id="8d208-121">必須</span><span class="sxs-lookup"><span data-stu-id="8d208-121">Required</span></span>  <br/> |<span data-ttu-id="8d208-122">**番号**</span><span class="sxs-lookup"><span data-stu-id="8d208-122">**Number**</span></span> <br/> | <span data-ttu-id="8d208-123">1 本目の線の [Angle] セルにある値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d208-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="8d208-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="8d208-124">_x2_</span></span> <br/> |<span data-ttu-id="8d208-125">必須</span><span class="sxs-lookup"><span data-stu-id="8d208-125">Required</span></span>  <br/> |<span data-ttu-id="8d208-126">**番号**</span><span class="sxs-lookup"><span data-stu-id="8d208-126">**Number**</span></span> <br/> |<span data-ttu-id="8d208-127">_X_の 2 番目の線上の点の座標です。</span><span class="sxs-lookup"><span data-stu-id="8d208-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="8d208-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="8d208-128">_y2_</span></span> <br/> |<span data-ttu-id="8d208-129">必須</span><span class="sxs-lookup"><span data-stu-id="8d208-129">Required</span></span>  <br/> |<span data-ttu-id="8d208-130">**番号**</span><span class="sxs-lookup"><span data-stu-id="8d208-130">**Number**</span></span> <br/> |<span data-ttu-id="8d208-131">_Y_の 2 つ目のライン上の点の座標です。</span><span class="sxs-lookup"><span data-stu-id="8d208-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="8d208-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="8d208-132">_angle2_</span></span> <br/> |<span data-ttu-id="8d208-133">必須</span><span class="sxs-lookup"><span data-stu-id="8d208-133">Required</span></span>  <br/> |<span data-ttu-id="8d208-134">**番号**</span><span class="sxs-lookup"><span data-stu-id="8d208-134">**Number**</span></span> <br/> |<span data-ttu-id="8d208-135">2 本目の線の [Angle] セルにある値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d208-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8d208-136">�߂�l</span><span class="sxs-lookup"><span data-stu-id="8d208-136">Return value</span></span>

<span data-ttu-id="8d208-137">数値</span><span class="sxs-lookup"><span data-stu-id="8d208-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d208-138">備考</span><span class="sxs-lookup"><span data-stu-id="8d208-138">Remarks</span></span>

<span data-ttu-id="8d208-139">各明細行は、点 (*x, y*) と角度として定義されます。</span><span class="sxs-lookup"><span data-stu-id="8d208-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="8d208-140">Microsoft Visio で、この関数は、回転したガイドに接着されている図形の [PinY] セルで使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d208-140">Microsoft Visio uses this function in the PinY cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="8d208-141">2 本の線が交差しない場合、この関数はゼロで除算したことを示すエラー (#DIV/0!) を返します。Visio ではこのエラーは無視され、最後に設定された点の座標値を復元します。</span><span class="sxs-lookup"><span data-stu-id="8d208-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8d208-142">例</span><span class="sxs-lookup"><span data-stu-id="8d208-142">Example</span></span>

<span data-ttu-id="8d208-143">INTERSECTY (VertGuide!VertGuide [pinx]![Piny]、VertGuide!HorzGuide の角度です。HorzGuide [pinx]![Piny]、HorzGuide!角度)</span><span class="sxs-lookup"><span data-stu-id="8d208-143">INTERSECTY(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="8d208-144">*Y*を返します-ページ単位での交差ポイントの VertGuide と HorzGuide の座標です。</span><span class="sxs-lookup"><span data-stu-id="8d208-144">Returns the  *y*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

