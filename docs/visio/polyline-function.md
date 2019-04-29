---
title: POLYLINE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: ポリラインを返します。 この関数は、[polylineto] geometry の行のセルで使用します。
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426297"
---
# <a name="polyline-function"></a><span data-ttu-id="80ae3-104">POLYLINE 関数</span><span class="sxs-lookup"><span data-stu-id="80ae3-104">POLYLINE Function</span></span>

<span data-ttu-id="80ae3-105">ポリラインを返します。</span><span class="sxs-lookup"><span data-stu-id="80ae3-105">Returns a polyline.</span></span> <span data-ttu-id="80ae3-106">この関数は、[polylineto] geometry の行のセルで使用します。</span><span class="sxs-lookup"><span data-stu-id="80ae3-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="80ae3-107">構文</span><span class="sxs-lookup"><span data-stu-id="80ae3-107">Syntax</span></span>

<span data-ttu-id="80ae3-108">ポリライン (\* \* *xType* \* *、* \* *yType* \* *、* \* *x1* \* *、* \* *y1* \* \*...)</span><span class="sxs-lookup"><span data-stu-id="80ae3-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="80ae3-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="80ae3-109">Parameters</span></span>

|<span data-ttu-id="80ae3-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="80ae3-110">**Name**</span></span>|<span data-ttu-id="80ae3-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="80ae3-111">**Required/Optional**</span></span>|<span data-ttu-id="80ae3-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="80ae3-112">**Data Type**</span></span>|<span data-ttu-id="80ae3-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="80ae3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="80ae3-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="80ae3-114">_xType_</span></span> <br/> |<span data-ttu-id="80ae3-115">必須</span><span class="sxs-lookup"><span data-stu-id="80ae3-115">Required</span></span>  <br/> |<span data-ttu-id="80ae3-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="80ae3-116">**Boolean**</span></span> <br/> |<span data-ttu-id="80ae3-117">_x_入力データを解釈する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="80ae3-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="80ae3-118">_xType_が0の場合、入力データ_x_は幅に対する割合として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="80ae3-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="80ae3-119">_xType_が1の場合、入力_x_データはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="80ae3-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="80ae3-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="80ae3-120">_yType_</span></span> <br/> |<span data-ttu-id="80ae3-121">必須</span><span class="sxs-lookup"><span data-stu-id="80ae3-121">Required</span></span>  <br/> |<span data-ttu-id="80ae3-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="80ae3-122">**Boolean**</span></span> <br/> |<span data-ttu-id="80ae3-123">_y_入力データの解釈方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="80ae3-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="80ae3-124">_yType_が0の場合、入力の_y_データは、高さの割合として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="80ae3-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="80ae3-125">_yType_が1の場合、入力の_y_データはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="80ae3-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="80ae3-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="80ae3-126">_x1_</span></span> <br/> |<span data-ttu-id="80ae3-127">必須</span><span class="sxs-lookup"><span data-stu-id="80ae3-127">Required</span></span>  <br/> |<span data-ttu-id="80ae3-128">**数値**</span><span class="sxs-lookup"><span data-stu-id="80ae3-128">**Number**</span></span> <br/> | <span data-ttu-id="80ae3-129">_x_座標を示します。</span><span class="sxs-lookup"><span data-stu-id="80ae3-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="80ae3-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="80ae3-130">_y1_</span></span> <br/> |<span data-ttu-id="80ae3-131">必須</span><span class="sxs-lookup"><span data-stu-id="80ae3-131">Required</span></span>  <br/> |<span data-ttu-id="80ae3-132">**数値**</span><span class="sxs-lookup"><span data-stu-id="80ae3-132">**Number**</span></span> <br/> |<span data-ttu-id="80ae3-133">_y_座標を示します。</span><span class="sxs-lookup"><span data-stu-id="80ae3-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80ae3-134">注釈</span><span class="sxs-lookup"><span data-stu-id="80ae3-134">Remarks</span></span>

<span data-ttu-id="80ae3-135">すべての*x*引数に対して、 *y*引数が必要です。それ以外の場合は、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="80ae3-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="80ae3-136">例</span><span class="sxs-lookup"><span data-stu-id="80ae3-136">Example</span></span>

<span data-ttu-id="80ae3-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="80ae3-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="80ae3-138">幅 x 高さの寸法の四角形を返します。</span><span class="sxs-lookup"><span data-stu-id="80ae3-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

