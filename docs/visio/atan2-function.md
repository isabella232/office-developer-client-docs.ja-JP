---
title: ATAN2 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: x、y、x 軸の方向によって表されるベクトル間の角度を返します。 角度を現在の単位で表した数値を取得できます。
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341483"
---
# <a name="atan2-function"></a><span data-ttu-id="e4111-104">ATAN2 関数</span><span class="sxs-lookup"><span data-stu-id="e4111-104">ATAN2 Function</span></span>

<span data-ttu-id="e4111-105">*x、y* 、 *x*軸の方向によって表されるベクトル間の角度を返します。</span><span class="sxs-lookup"><span data-stu-id="e4111-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="e4111-106">角度を現在の単位で表した数値を取得できます。</span><span class="sxs-lookup"><span data-stu-id="e4111-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e4111-107">構文</span><span class="sxs-lookup"><span data-stu-id="e4111-107">Syntax</span></span>

<span data-ttu-id="e4111-108">ATAN2 (\* \* *y* \* *、* \* *x* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e4111-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e4111-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e4111-109">Parameters</span></span>

|<span data-ttu-id="e4111-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="e4111-110">**Name**</span></span>|<span data-ttu-id="e4111-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e4111-111">**Required/Optional**</span></span>|<span data-ttu-id="e4111-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e4111-112">**Data Type**</span></span>|<span data-ttu-id="e4111-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="e4111-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e4111-114">_y_</span><span class="sxs-lookup"><span data-stu-id="e4111-114">_y_</span></span> <br/> |<span data-ttu-id="e4111-115">必須</span><span class="sxs-lookup"><span data-stu-id="e4111-115">Required</span></span>  <br/> |<span data-ttu-id="e4111-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="e4111-116">**Numeric**</span></span> <br/> |<span data-ttu-id="e4111-117">点の_y_値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4111-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="e4111-118">_x_</span><span class="sxs-lookup"><span data-stu-id="e4111-118">_x_</span></span> <br/> |<span data-ttu-id="e4111-119">必須</span><span class="sxs-lookup"><span data-stu-id="e4111-119">Required</span></span>  <br/> |<span data-ttu-id="e4111-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="e4111-120">**Numeric**</span></span> <br/> |<span data-ttu-id="e4111-121">点の_x_値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4111-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4111-122">解説</span><span class="sxs-lookup"><span data-stu-id="e4111-122">Remarks</span></span>

<span data-ttu-id="e4111-123">アークタンジェントは、正の*x*軸から、原点 (0, 0) と、 *x*と*y*で表される点を交差する直線までの角度を反時計回りに表したものです。</span><span class="sxs-lookup"><span data-stu-id="e4111-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="e4111-124">Microsoft Visio では、ATAN2(0,0) は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="e4111-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="e4111-125">ATAN2 の結果を、角度に関する別の測定方法に適用するには、DEG または RAD 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="e4111-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="e4111-126">ATAN2 関数は TAN 関数の逆関数になります。</span><span class="sxs-lookup"><span data-stu-id="e4111-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="e4111-127">ATAN2 関数は、y を*x*で割ると、角度が*y*に等しい角度を返します。</span><span class="sxs-lookup"><span data-stu-id="e4111-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="e4111-128">atan2 (*y, x*) が直角三角形の角度を表している場合、 *y*は "反対側"、 *x*は "隣接側" となり、関数は ATAN2 (反対、隣接) として記述されます。</span><span class="sxs-lookup"><span data-stu-id="e4111-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e4111-129">例 1</span><span class="sxs-lookup"><span data-stu-id="e4111-129">Example 1</span></span>

<span data-ttu-id="e4111-130">ATAN2 (1.25、2.25)</span><span class="sxs-lookup"><span data-stu-id="e4111-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="e4111-131">29.0456°を返します</span><span class="sxs-lookup"><span data-stu-id="e4111-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e4111-132">例 2</span><span class="sxs-lookup"><span data-stu-id="e4111-132">Example 2</span></span>

<span data-ttu-id="e4111-133">ATAN2 (1, SQRT (3))</span><span class="sxs-lookup"><span data-stu-id="e4111-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="e4111-134">30°を返します</span><span class="sxs-lookup"><span data-stu-id="e4111-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e4111-135">例 3</span><span class="sxs-lookup"><span data-stu-id="e4111-135">Example 3</span></span>

<span data-ttu-id="e4111-136">ATAN2 (1, 1)</span><span class="sxs-lookup"><span data-stu-id="e4111-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="e4111-137">45°を返します</span><span class="sxs-lookup"><span data-stu-id="e4111-137">Returns 45 deg</span></span>
  

