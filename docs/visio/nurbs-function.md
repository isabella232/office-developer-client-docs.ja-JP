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
description: 非一次有理 B スプライン (NURBS) を返します。 この関数は、NURBSTo ジオメトリ行の E セルで使用されます。
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438457"
---
# <a name="nurbs-function"></a><span data-ttu-id="2238e-104">NURBS 関数</span><span class="sxs-lookup"><span data-stu-id="2238e-104">NURBS Function</span></span>

<span data-ttu-id="2238e-105">非一次有理 B スプライン (NURBS) を返します。</span><span class="sxs-lookup"><span data-stu-id="2238e-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="2238e-106">この関数は、NURBSTo ジオメトリ行の E セルで使用されます。</span><span class="sxs-lookup"><span data-stu-id="2238e-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2238e-107">構文</span><span class="sxs-lookup"><span data-stu-id="2238e-107">Syntax</span></span>

<span data-ttu-id="2238e-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* xType \*\*, \*\* *yType* \*\*, \*\* x1 \*\*,  \*\* *y1* \*\*, \*\* knot1 \*\*, \*\*  *weight1* \*\*, ..) </span><span class="sxs-lookup"><span data-stu-id="2238e-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2238e-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2238e-109">Parameters</span></span>

|<span data-ttu-id="2238e-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="2238e-110">**Name**</span></span>|<span data-ttu-id="2238e-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="2238e-111">**Required/Optional**</span></span>|<span data-ttu-id="2238e-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="2238e-112">**Data Type**</span></span>|<span data-ttu-id="2238e-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="2238e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2238e-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="2238e-114">_knotLast_</span></span> <br/> |<span data-ttu-id="2238e-115">必須</span><span class="sxs-lookup"><span data-stu-id="2238e-115">Required</span></span>  <br/> |<span data-ttu-id="2238e-116">**string**</span><span class="sxs-lookup"><span data-stu-id="2238e-116">**string**</span></span> <br/> | <span data-ttu-id="2238e-117">最後のノットを指定します。</span><span class="sxs-lookup"><span data-stu-id="2238e-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="2238e-118">_度_</span><span class="sxs-lookup"><span data-stu-id="2238e-118">_degree_</span></span> <br/> |<span data-ttu-id="2238e-119">必須</span><span class="sxs-lookup"><span data-stu-id="2238e-119">Required</span></span>  <br/> |<span data-ttu-id="2238e-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="2238e-120">**Numeric**</span></span> <br/> |<span data-ttu-id="2238e-121">スプラインの角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="2238e-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="2238e-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="2238e-122">_xType_</span></span> <br/> |<span data-ttu-id="2238e-123">必須</span><span class="sxs-lookup"><span data-stu-id="2238e-123">Required</span></span>  <br/> |<span data-ttu-id="2238e-124">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="2238e-124">**Numeric**</span></span> <br/> |<span data-ttu-id="2238e-125">x 入力データの解釈方法  _を_ 指定します。</span><span class="sxs-lookup"><span data-stu-id="2238e-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="2238e-126">_xType が_ 0 の場合、_すべての x_ 入力データは Width のパーセンテージとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="2238e-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="2238e-127">_xType が_ 1 の場合、_すべての x_ 入力データはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="2238e-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="2238e-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="2238e-128">_yType_</span></span> <br/> |<span data-ttu-id="2238e-129">必須</span><span class="sxs-lookup"><span data-stu-id="2238e-129">Required</span></span>  <br/> |<span data-ttu-id="2238e-130">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="2238e-130">**Numeric**</span></span> <br/> |<span data-ttu-id="2238e-131">y 入力データの  _解釈方法を_ 指定します。</span><span class="sxs-lookup"><span data-stu-id="2238e-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="2238e-132">_yType が_ 0 の場合、_すべての y_ 入力データは Height のパーセンテージとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="2238e-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="2238e-133">_yType が_ 1 の場合、_すべての y_ 入力データはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="2238e-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="2238e-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="2238e-134">_x1_</span></span> <br/> |<span data-ttu-id="2238e-135">必須</span><span class="sxs-lookup"><span data-stu-id="2238e-135">Required</span></span>  <br/> |<span data-ttu-id="2238e-136">**String**</span><span class="sxs-lookup"><span data-stu-id="2238e-136">**String**</span></span> <br/> |<span data-ttu-id="2238e-137">x 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="2238e-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="2238e-138">_y1_</span><span class="sxs-lookup"><span data-stu-id="2238e-138">_y1_</span></span> <br/> |<span data-ttu-id="2238e-139">必須</span><span class="sxs-lookup"><span data-stu-id="2238e-139">Required</span></span>  <br/> |<span data-ttu-id="2238e-140">**String**</span><span class="sxs-lookup"><span data-stu-id="2238e-140">**String**</span></span> <br/> |<span data-ttu-id="2238e-141">y 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="2238e-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="2238e-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="2238e-142">_knot1_</span></span> <br/> |<span data-ttu-id="2238e-143">必須</span><span class="sxs-lookup"><span data-stu-id="2238e-143">Required</span></span>  <br/> |<span data-ttu-id="2238e-144">**String**</span><span class="sxs-lookup"><span data-stu-id="2238e-144">**String**</span></span> <br/> |<span data-ttu-id="2238e-145">B スプライン上のノットを指定します。</span><span class="sxs-lookup"><span data-stu-id="2238e-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="2238e-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="2238e-146">_weight1_</span></span> <br/> |<span data-ttu-id="2238e-147">必須</span><span class="sxs-lookup"><span data-stu-id="2238e-147">Required</span></span>  <br/> |<span data-ttu-id="2238e-148">**String**</span><span class="sxs-lookup"><span data-stu-id="2238e-148">**String**</span></span> <br/> |<span data-ttu-id="2238e-149">B スプラインの太さを指定します。</span><span class="sxs-lookup"><span data-stu-id="2238e-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2238e-150">注釈</span><span class="sxs-lookup"><span data-stu-id="2238e-150">Remarks</span></span>

<span data-ttu-id="2238e-151">x 引数  *ごとに y*  引数  *が必要*  です。それ以外の場合は、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="2238e-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="2238e-152">少なくとも 1 つの *x、y*、ノット、*および weight* 引数を *指定する必要* があります。それ以外の場合Visioエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="2238e-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

