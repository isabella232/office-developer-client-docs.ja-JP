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
description: ポリラインを返します。 この関数は、PolyLineTo ジオメトリ行の [A] セルで使用されます。
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426297"
---
# <a name="polyline-function"></a><span data-ttu-id="8d829-104">POLYLINE 関数</span><span class="sxs-lookup"><span data-stu-id="8d829-104">POLYLINE Function</span></span>

<span data-ttu-id="8d829-105">ポリラインを返します。</span><span class="sxs-lookup"><span data-stu-id="8d829-105">Returns a polyline.</span></span> <span data-ttu-id="8d829-106">この関数は、PolyLineTo ジオメトリ行の [A] セルで使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d829-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d829-107">構文</span><span class="sxs-lookup"><span data-stu-id="8d829-107">Syntax</span></span>

<span data-ttu-id="8d829-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*..)</span><span class="sxs-lookup"><span data-stu-id="8d829-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d829-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d829-109">Parameters</span></span>

|<span data-ttu-id="8d829-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="8d829-110">**Name**</span></span>|<span data-ttu-id="8d829-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="8d829-111">**Required/Optional**</span></span>|<span data-ttu-id="8d829-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="8d829-112">**Data Type**</span></span>|<span data-ttu-id="8d829-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="8d829-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d829-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="8d829-114">_xType_</span></span> <br/> |<span data-ttu-id="8d829-115">必須</span><span class="sxs-lookup"><span data-stu-id="8d829-115">Required</span></span>  <br/> |<span data-ttu-id="8d829-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8d829-116">**Boolean**</span></span> <br/> |<span data-ttu-id="8d829-117">x 入力データの解釈方法  _を_ 指定します。</span><span class="sxs-lookup"><span data-stu-id="8d829-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="8d829-118">_xType が_ 0 の場合、入力 _x_-data は Width のパーセンテージとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="8d829-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="8d829-119">_xType が_ 1 の場合、入力 _x_-data はローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="8d829-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="8d829-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="8d829-120">_yType_</span></span> <br/> |<span data-ttu-id="8d829-121">必須</span><span class="sxs-lookup"><span data-stu-id="8d829-121">Required</span></span>  <br/> |<span data-ttu-id="8d829-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8d829-122">**Boolean**</span></span> <br/> |<span data-ttu-id="8d829-123">y -input データの  _解釈方法_ を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d829-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="8d829-124">_yType が_ 0 の場合、入力 _y_-data は Height のパーセンテージとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="8d829-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="8d829-125">_yType が_ 1 の場合、入力 _y_-data はローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="8d829-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="8d829-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="8d829-126">_x1_</span></span> <br/> |<span data-ttu-id="8d829-127">必須</span><span class="sxs-lookup"><span data-stu-id="8d829-127">Required</span></span>  <br/> |<span data-ttu-id="8d829-128">**数値**</span><span class="sxs-lookup"><span data-stu-id="8d829-128">**Number**</span></span> <br/> | <span data-ttu-id="8d829-129">_x_ 座標。</span><span class="sxs-lookup"><span data-stu-id="8d829-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="8d829-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="8d829-130">_y1_</span></span> <br/> |<span data-ttu-id="8d829-131">必須</span><span class="sxs-lookup"><span data-stu-id="8d829-131">Required</span></span>  <br/> |<span data-ttu-id="8d829-132">**数値**</span><span class="sxs-lookup"><span data-stu-id="8d829-132">**Number**</span></span> <br/> |<span data-ttu-id="8d829-133">_y_ 座標。</span><span class="sxs-lookup"><span data-stu-id="8d829-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d829-134">注釈</span><span class="sxs-lookup"><span data-stu-id="8d829-134">Remarks</span></span>

<span data-ttu-id="8d829-135">x 引数  *ごとに y*  引数  *が必要*  です。それ以外の場合は、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="8d829-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8d829-136">例</span><span class="sxs-lookup"><span data-stu-id="8d829-136">Example</span></span>

<span data-ttu-id="8d829-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="8d829-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="8d829-138">幅 x 高さの寸法の四角形を返します。</span><span class="sxs-lookup"><span data-stu-id="8d829-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

