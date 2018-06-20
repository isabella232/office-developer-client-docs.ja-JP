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
description: ポリラインを返します。 PolyLineTo ジオメトリの行のセルには、この関数が使用されます。
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806012"
---
# <a name="polyline-function"></a><span data-ttu-id="7ad61-104">POLYLINE 関数</span><span class="sxs-lookup"><span data-stu-id="7ad61-104">POLYLINE Function</span></span>

<span data-ttu-id="7ad61-105">ポリラインを返します。</span><span class="sxs-lookup"><span data-stu-id="7ad61-105">Returns a polyline.</span></span> <span data-ttu-id="7ad61-106">PolyLineTo ジオメトリの行のセルには、この関数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ad61-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7ad61-107">構文</span><span class="sxs-lookup"><span data-stu-id="7ad61-107">Syntax</span></span>

<span data-ttu-id="7ad61-108">ポリライン (* * *xType* * *、* * *yType* * *、* * *x1* * *、* * *y1* * *.)</span><span class="sxs-lookup"><span data-stu-id="7ad61-108">POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7ad61-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="7ad61-109">Parameters</span></span>

|<span data-ttu-id="7ad61-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="7ad61-110">**Name**</span></span>|<span data-ttu-id="7ad61-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="7ad61-111">**Required/Optional**</span></span>|<span data-ttu-id="7ad61-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="7ad61-112">**Data Type**</span></span>|<span data-ttu-id="7ad61-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="7ad61-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7ad61-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="7ad61-114">_xType_</span></span> <br/> |<span data-ttu-id="7ad61-115">必須</span><span class="sxs-lookup"><span data-stu-id="7ad61-115">Required</span></span>  <br/> |<span data-ttu-id="7ad61-116">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="7ad61-116">**Boolean**</span></span> <br/> |<span data-ttu-id="7ad61-117">_X_の入力データを解釈する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="7ad61-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="7ad61-118">_XType_が 0 で、 _x_の入力のかどうかのデータの幅に対する割合として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="7ad61-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="7ad61-119">_XType_が 1、入力_x_のかどうか、データはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="7ad61-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="7ad61-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="7ad61-120">_yType_</span></span> <br/> |<span data-ttu-id="7ad61-121">必須</span><span class="sxs-lookup"><span data-stu-id="7ad61-121">Required</span></span>  <br/> |<span data-ttu-id="7ad61-122">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="7ad61-122">**Boolean**</span></span> <br/> |<span data-ttu-id="7ad61-123">_Y_の解釈方法を指定のデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="7ad61-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="7ad61-124">_YType_が 0、 _y_の入力のかどうかのデータは高さに対する割合として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="7ad61-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="7ad61-125">_YType_が 1、 _y_の入力のかどうか、データはローカル座標として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="7ad61-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="7ad61-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="7ad61-126">_x1_</span></span> <br/> |<span data-ttu-id="7ad61-127">必須</span><span class="sxs-lookup"><span data-stu-id="7ad61-127">Required</span></span>  <br/> |<span data-ttu-id="7ad61-128">**番号**</span><span class="sxs-lookup"><span data-stu-id="7ad61-128">**Number**</span></span> <br/> | <span data-ttu-id="7ad61-129">_X_を調整します。</span><span class="sxs-lookup"><span data-stu-id="7ad61-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="7ad61-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="7ad61-130">_y1_</span></span> <br/> |<span data-ttu-id="7ad61-131">必須</span><span class="sxs-lookup"><span data-stu-id="7ad61-131">Required</span></span>  <br/> |<span data-ttu-id="7ad61-132">**番号**</span><span class="sxs-lookup"><span data-stu-id="7ad61-132">**Number**</span></span> <br/> |<span data-ttu-id="7ad61-133">_Y_の座標です。</span><span class="sxs-lookup"><span data-stu-id="7ad61-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ad61-134">備考</span><span class="sxs-lookup"><span data-stu-id="7ad61-134">Remarks</span></span>

<span data-ttu-id="7ad61-135">すべての*x*引数では、必要があります、 *y*引数を指定します。それ以外の場合、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="7ad61-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7ad61-136">例</span><span class="sxs-lookup"><span data-stu-id="7ad61-136">Example</span></span>

<span data-ttu-id="7ad61-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="7ad61-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="7ad61-138">幅 x 高さの寸法の四角形を返します。</span><span class="sxs-lookup"><span data-stu-id="7ad61-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

