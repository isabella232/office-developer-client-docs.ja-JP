---
title: NURBS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: 不均一な合理性のある B スプライン (NURBS) を返します。 [Nurbsto] のジオメトリの行の [E] セルでは、この関数が使用されます。
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805965"
---
# <a name="nurbs-function"></a><span data-ttu-id="4a0e6-104">NURBS 関数</span><span class="sxs-lookup"><span data-stu-id="4a0e6-104">NURBS Function</span></span>

<span data-ttu-id="4a0e6-105">不均一な合理性のある B スプライン (NURBS) を返します。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="4a0e6-106">[Nurbsto] のジオメトリの行の [E] セルでは、この関数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4a0e6-107">構文</span><span class="sxs-lookup"><span data-stu-id="4a0e6-107">Syntax</span></span>

<span data-ttu-id="4a0e6-108">NURBS (* * *knotLast* * *、* **度** *、* * *xType* * *、* * *yType* * *、* * *x1* * *、* * *y1* * *、* * *knot1* * *、* * *weight1* * *,...)</span><span class="sxs-lookup"><span data-stu-id="4a0e6-108">NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4a0e6-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="4a0e6-109">Parameters</span></span>

|<span data-ttu-id="4a0e6-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-110">**Name**</span></span>|<span data-ttu-id="4a0e6-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-111">**Required/Optional**</span></span>|<span data-ttu-id="4a0e6-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-112">**Data Type**</span></span>|<span data-ttu-id="4a0e6-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4a0e6-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="4a0e6-114">_knotLast_</span></span> <br/> |<span data-ttu-id="4a0e6-115">必須</span><span class="sxs-lookup"><span data-stu-id="4a0e6-115">Required</span></span>  <br/> |<span data-ttu-id="4a0e6-116">**string**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-116">**string**</span></span> <br/> | <span data-ttu-id="4a0e6-117">最後のノットを指定します。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="4a0e6-118">_度_</span><span class="sxs-lookup"><span data-stu-id="4a0e6-118">_degree_</span></span> <br/> |<span data-ttu-id="4a0e6-119">必須</span><span class="sxs-lookup"><span data-stu-id="4a0e6-119">Required</span></span>  <br/> |<span data-ttu-id="4a0e6-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-120">**Numeric**</span></span> <br/> |<span data-ttu-id="4a0e6-121">スプラインの角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="4a0e6-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="4a0e6-122">_xType_</span></span> <br/> |<span data-ttu-id="4a0e6-123">必須</span><span class="sxs-lookup"><span data-stu-id="4a0e6-123">Required</span></span>  <br/> |<span data-ttu-id="4a0e6-124">**数値**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-124">**Numeric**</span></span> <br/> |<span data-ttu-id="4a0e6-125">_X_の入力データを解釈する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="4a0e6-126">_XType_が 0 の場合は、入力データ_x_のすべては幅に対する割合として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="4a0e6-127">_XType_が 1 の場合は、入力データ_x_のすべてはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="4a0e6-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="4a0e6-128">_yType_</span></span> <br/> |<span data-ttu-id="4a0e6-129">必須</span><span class="sxs-lookup"><span data-stu-id="4a0e6-129">Required</span></span>  <br/> |<span data-ttu-id="4a0e6-130">**数値**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-130">**Numeric**</span></span> <br/> |<span data-ttu-id="4a0e6-131">入力データ_y_の解釈方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="4a0e6-132">_YType_が 0 の場合は、入力データ_y_のすべては高さに対する割合として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="4a0e6-133">_YType_が 1 の場合は、入力データ_y_のすべてはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="4a0e6-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="4a0e6-134">_x1_</span></span> <br/> |<span data-ttu-id="4a0e6-135">必須</span><span class="sxs-lookup"><span data-stu-id="4a0e6-135">Required</span></span>  <br/> |<span data-ttu-id="4a0e6-136">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-136">**String**</span></span> <br/> |<span data-ttu-id="4a0e6-137">x 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="4a0e6-138">_y1_</span><span class="sxs-lookup"><span data-stu-id="4a0e6-138">_y1_</span></span> <br/> |<span data-ttu-id="4a0e6-139">必須</span><span class="sxs-lookup"><span data-stu-id="4a0e6-139">Required</span></span>  <br/> |<span data-ttu-id="4a0e6-140">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-140">**String**</span></span> <br/> |<span data-ttu-id="4a0e6-141">y 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="4a0e6-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="4a0e6-142">_knot1_</span></span> <br/> |<span data-ttu-id="4a0e6-143">必須</span><span class="sxs-lookup"><span data-stu-id="4a0e6-143">Required</span></span>  <br/> |<span data-ttu-id="4a0e6-144">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-144">**String**</span></span> <br/> |<span data-ttu-id="4a0e6-145">B スプライン上のノットを指定します。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="4a0e6-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="4a0e6-146">_weight1_</span></span> <br/> |<span data-ttu-id="4a0e6-147">必須</span><span class="sxs-lookup"><span data-stu-id="4a0e6-147">Required</span></span>  <br/> |<span data-ttu-id="4a0e6-148">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4a0e6-148">**String**</span></span> <br/> |<span data-ttu-id="4a0e6-149">B スプラインの太さを指定します。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a0e6-150">注釈</span><span class="sxs-lookup"><span data-stu-id="4a0e6-150">Remarks</span></span>

<span data-ttu-id="4a0e6-151">すべての*x*引数では、必要があります、 *y*引数を指定します。それ以外の場合、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="4a0e6-152">少なくとも 1 つの*x*、 *y*、*ノット*、および*重量*の引数を指定する必要があります。それ以外の場合、Visio では、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="4a0e6-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

