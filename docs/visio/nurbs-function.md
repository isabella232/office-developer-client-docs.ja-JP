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
description: 一様でない有理数 B スプライン (NURBS) を返します。 この関数は、[nurbsto] geometry 行の E セルで使用されます。
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438457"
---
# <a name="nurbs-function"></a><span data-ttu-id="21a45-104">NURBS 関数</span><span class="sxs-lookup"><span data-stu-id="21a45-104">NURBS Function</span></span>

<span data-ttu-id="21a45-105">一様でない有理数 B スプライン (NURBS) を返します。</span><span class="sxs-lookup"><span data-stu-id="21a45-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="21a45-106">この関数は、[nurbsto] geometry 行の E セルで使用されます。</span><span class="sxs-lookup"><span data-stu-id="21a45-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="21a45-107">構文</span><span class="sxs-lookup"><span data-stu-id="21a45-107">Syntax</span></span>

<span data-ttu-id="21a45-108">NURBS (\* \* *knotLast* \* *、* **度** *、* \* *xType* \* *、* \* *yType* \* *、* \* *x1* \* *、* \* *y1* \* *、* \* *knot1* \* *、* \* *weight1* \* \*、...)</span><span class="sxs-lookup"><span data-stu-id="21a45-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="21a45-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21a45-109">Parameters</span></span>

|<span data-ttu-id="21a45-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="21a45-110">**Name**</span></span>|<span data-ttu-id="21a45-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="21a45-111">**Required/Optional**</span></span>|<span data-ttu-id="21a45-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="21a45-112">**Data Type**</span></span>|<span data-ttu-id="21a45-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="21a45-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="21a45-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="21a45-114">_knotLast_</span></span> <br/> |<span data-ttu-id="21a45-115">必須</span><span class="sxs-lookup"><span data-stu-id="21a45-115">Required</span></span>  <br/> |<span data-ttu-id="21a45-116">**string**</span><span class="sxs-lookup"><span data-stu-id="21a45-116">**string**</span></span> <br/> | <span data-ttu-id="21a45-117">最後のノットを指定します。</span><span class="sxs-lookup"><span data-stu-id="21a45-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="21a45-118">_度合_</span><span class="sxs-lookup"><span data-stu-id="21a45-118">_degree_</span></span> <br/> |<span data-ttu-id="21a45-119">必須</span><span class="sxs-lookup"><span data-stu-id="21a45-119">Required</span></span>  <br/> |<span data-ttu-id="21a45-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="21a45-120">**Numeric**</span></span> <br/> |<span data-ttu-id="21a45-121">スプラインの角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="21a45-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="21a45-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="21a45-122">_xType_</span></span> <br/> |<span data-ttu-id="21a45-123">必須</span><span class="sxs-lookup"><span data-stu-id="21a45-123">Required</span></span>  <br/> |<span data-ttu-id="21a45-124">**数値**</span><span class="sxs-lookup"><span data-stu-id="21a45-124">**Numeric**</span></span> <br/> |<span data-ttu-id="21a45-125">_x_入力データを解釈する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="21a45-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="21a45-126">_xType_が0の場合、すべての_x_入力データは幅に対する割合として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="21a45-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="21a45-127">_xType_が1の場合、すべての_x_入力データはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="21a45-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="21a45-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="21a45-128">_yType_</span></span> <br/> |<span data-ttu-id="21a45-129">必須</span><span class="sxs-lookup"><span data-stu-id="21a45-129">Required</span></span>  <br/> |<span data-ttu-id="21a45-130">**数値**</span><span class="sxs-lookup"><span data-stu-id="21a45-130">**Numeric**</span></span> <br/> |<span data-ttu-id="21a45-131">_y_入力データの解釈方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="21a45-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="21a45-132">_yType_が0の場合、すべての_y_入力データは、高さの割合として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="21a45-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="21a45-133">_yType_が1の場合、すべての_y_入力データはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="21a45-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="21a45-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="21a45-134">_x1_</span></span> <br/> |<span data-ttu-id="21a45-135">必須</span><span class="sxs-lookup"><span data-stu-id="21a45-135">Required</span></span>  <br/> |<span data-ttu-id="21a45-136">**String**</span><span class="sxs-lookup"><span data-stu-id="21a45-136">**String**</span></span> <br/> |<span data-ttu-id="21a45-137">x 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="21a45-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="21a45-138">_y1_</span><span class="sxs-lookup"><span data-stu-id="21a45-138">_y1_</span></span> <br/> |<span data-ttu-id="21a45-139">必須</span><span class="sxs-lookup"><span data-stu-id="21a45-139">Required</span></span>  <br/> |<span data-ttu-id="21a45-140">**String**</span><span class="sxs-lookup"><span data-stu-id="21a45-140">**String**</span></span> <br/> |<span data-ttu-id="21a45-141">y 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="21a45-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="21a45-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="21a45-142">_knot1_</span></span> <br/> |<span data-ttu-id="21a45-143">必須</span><span class="sxs-lookup"><span data-stu-id="21a45-143">Required</span></span>  <br/> |<span data-ttu-id="21a45-144">**String**</span><span class="sxs-lookup"><span data-stu-id="21a45-144">**String**</span></span> <br/> |<span data-ttu-id="21a45-145">B スプライン上のノットを指定します。</span><span class="sxs-lookup"><span data-stu-id="21a45-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="21a45-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="21a45-146">_weight1_</span></span> <br/> |<span data-ttu-id="21a45-147">必須</span><span class="sxs-lookup"><span data-stu-id="21a45-147">Required</span></span>  <br/> |<span data-ttu-id="21a45-148">**String**</span><span class="sxs-lookup"><span data-stu-id="21a45-148">**String**</span></span> <br/> |<span data-ttu-id="21a45-149">B スプラインの太さを指定します。</span><span class="sxs-lookup"><span data-stu-id="21a45-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21a45-150">注釈</span><span class="sxs-lookup"><span data-stu-id="21a45-150">Remarks</span></span>

<span data-ttu-id="21a45-151">すべての*x*引数に対して、 *y*引数が必要です。それ以外の場合は、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="21a45-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="21a45-152">少なくとも1つの*x*、 *y*、*ノット*、および*weight*引数を指定する必要があります。それ以外の場合、Visio はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="21a45-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

