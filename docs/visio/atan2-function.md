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
description: X によって表されるベクトルの角度を返します。 y、x 方向の軸。 角度の測定の現在の単位の数値になります。
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804772"
---
# <a name="atan2-function"></a><span data-ttu-id="05631-104">ATAN2 関数</span><span class="sxs-lookup"><span data-stu-id="05631-104">ATAN2 Function</span></span>

<span data-ttu-id="05631-105">*X、y*および*x*の方向によって表されるベクトルの角度を返します-軸です。</span><span class="sxs-lookup"><span data-stu-id="05631-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="05631-106">角度の測定の現在の単位の数値になります。</span><span class="sxs-lookup"><span data-stu-id="05631-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="05631-107">構文</span><span class="sxs-lookup"><span data-stu-id="05631-107">Syntax</span></span>

<span data-ttu-id="05631-108">ATAN2 (* * *y* * *、* * *x* * *)</span><span class="sxs-lookup"><span data-stu-id="05631-108">ATAN2(** *y* **, ** *x* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="05631-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="05631-109">Parameters</span></span>

|<span data-ttu-id="05631-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="05631-110">**Name**</span></span>|<span data-ttu-id="05631-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="05631-111">**Required/Optional**</span></span>|<span data-ttu-id="05631-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="05631-112">**Data Type**</span></span>|<span data-ttu-id="05631-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="05631-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="05631-114">_y_</span><span class="sxs-lookup"><span data-stu-id="05631-114">_y_</span></span> <br/> |<span data-ttu-id="05631-115">必須</span><span class="sxs-lookup"><span data-stu-id="05631-115">Required</span></span>  <br/> |<span data-ttu-id="05631-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="05631-116">**Numeric**</span></span> <br/> |<span data-ttu-id="05631-117">_Y_-点の値です。</span><span class="sxs-lookup"><span data-stu-id="05631-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="05631-118">_x_</span><span class="sxs-lookup"><span data-stu-id="05631-118">_x_</span></span> <br/> |<span data-ttu-id="05631-119">必須</span><span class="sxs-lookup"><span data-stu-id="05631-119">Required</span></span>  <br/> |<span data-ttu-id="05631-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="05631-120">**Numeric**</span></span> <br/> |<span data-ttu-id="05631-121">_X_-点の値です。</span><span class="sxs-lookup"><span data-stu-id="05631-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05631-122">注釈</span><span class="sxs-lookup"><span data-stu-id="05631-122">Remarks</span></span>

<span data-ttu-id="05631-123">アーク タンジェントは、正の*x*から反時計回りに測定する角度の原点 (0, 0) および*x*と*y*で表される点を通る直線を軸。</span><span class="sxs-lookup"><span data-stu-id="05631-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="05631-124">Microsoft Visio では、ATAN2(0,0) は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="05631-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="05631-125">ATAN2 の結果を別の角度の測定を強制するには、DEG または RAD 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="05631-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="05631-126">ATAN2 関数は、TAN 関数の antifunction です。</span><span class="sxs-lookup"><span data-stu-id="05631-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="05631-127">ATAN2 関数が返す角度は、 *y*を*x*で割った値に等しい角度です。</span><span class="sxs-lookup"><span data-stu-id="05631-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="05631-128">場合 ATAN2 (*y, x*) は、直角三角形の角度を表す、 *y*は「反対側の辺」、および atan2 関数が書き込まれるために、 *x*は「隣接する辺」。</span><span class="sxs-lookup"><span data-stu-id="05631-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="05631-129">例 1</span><span class="sxs-lookup"><span data-stu-id="05631-129">Example 1</span></span>

<span data-ttu-id="05631-130">ATAN2(1.25,2.25)</span><span class="sxs-lookup"><span data-stu-id="05631-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="05631-131">29.0456°を返します</span><span class="sxs-lookup"><span data-stu-id="05631-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="05631-132">例 2</span><span class="sxs-lookup"><span data-stu-id="05631-132">Example 2</span></span>

<span data-ttu-id="05631-133">ATAN2(1,SQRT(3))</span><span class="sxs-lookup"><span data-stu-id="05631-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="05631-134">30°を返します</span><span class="sxs-lookup"><span data-stu-id="05631-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="05631-135">例 3</span><span class="sxs-lookup"><span data-stu-id="05631-135">Example 3</span></span>

<span data-ttu-id="05631-136">ATAN2(1,1)</span><span class="sxs-lookup"><span data-stu-id="05631-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="05631-137">45°を返します</span><span class="sxs-lookup"><span data-stu-id="05631-137">Returns 45 deg</span></span>
  

