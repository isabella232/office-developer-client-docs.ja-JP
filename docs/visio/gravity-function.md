---
title: GRAVITY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: テキスト ブロックの正確なテキストの上下が逆にならないようにするのには指定された図形の回転の回転角度を計算します。
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805487"
---
# <a name="gravity-function"></a><span data-ttu-id="bc3b6-103">GRAVITY 関数</span><span class="sxs-lookup"><span data-stu-id="bc3b6-103">GRAVITY Function</span></span>

<span data-ttu-id="bc3b6-104">テキスト ブロックの正確なテキストの上下が逆にならないようにするのには指定された図形の回転の回転角度を計算します。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bc3b6-105">構文</span><span class="sxs-lookup"><span data-stu-id="bc3b6-105">Syntax</span></span>

<span data-ttu-id="bc3b6-106">重力加速度 (* **角度** *、[* * *limit1* * *]、[* * *limit2* * *])</span><span class="sxs-lookup"><span data-stu-id="bc3b6-106">GRAVITY(** *angle* **,[ ** *limit1* ** ],[ ** *limit2* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bc3b6-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="bc3b6-107">Parameters</span></span>

|<span data-ttu-id="bc3b6-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="bc3b6-108">**Name**</span></span>|<span data-ttu-id="bc3b6-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="bc3b6-109">**Required/Optional**</span></span>|<span data-ttu-id="bc3b6-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="bc3b6-110">**Data Type**</span></span>|<span data-ttu-id="bc3b6-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="bc3b6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bc3b6-112">_角度_</span><span class="sxs-lookup"><span data-stu-id="bc3b6-112">_angle_</span></span> <br/> |<span data-ttu-id="bc3b6-113">必須</span><span class="sxs-lookup"><span data-stu-id="bc3b6-113">Required</span></span>  <br/> |<span data-ttu-id="bc3b6-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="bc3b6-114">**String**</span></span> <br/> | <span data-ttu-id="bc3b6-115">図形の角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="bc3b6-116">_limit1_</span><span class="sxs-lookup"><span data-stu-id="bc3b6-116">_limit1_</span></span> <br/> |<span data-ttu-id="bc3b6-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="bc3b6-117">Optional</span></span>  <br/> |<span data-ttu-id="bc3b6-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="bc3b6-118">**String**</span></span> <br/> |<span data-ttu-id="bc3b6-p101">回転の最初の制限角度を指定します。既定の制限角度は 90°です。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-p101">First limit of rotation. Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="bc3b6-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="bc3b6-121">_limit2_</span></span> <br/> |<span data-ttu-id="bc3b6-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="bc3b6-122">Optional</span></span>  <br/> |<span data-ttu-id="bc3b6-123">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="bc3b6-123">**String**</span></span> <br/> |<span data-ttu-id="bc3b6-p102">回転の 2 番目の制限角度を指定します。既定の制限角度は 270°です。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-p102">Second limit of rotation. Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bc3b6-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bc3b6-126">Return value</span></span>

<span data-ttu-id="bc3b6-127">文字列</span><span class="sxs-lookup"><span data-stu-id="bc3b6-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc3b6-128">注釈</span><span class="sxs-lookup"><span data-stu-id="bc3b6-128">Remarks</span></span>

<span data-ttu-id="bc3b6-129">通常、GRAVITY 関数は [TxtAngle] セルで使用します。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="bc3b6-130">_Limit1_および_limit2_; で指定された値の間_の角度_の場合、返される値は 180 度それ以外の場合戻り値は、0 度です。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="bc3b6-p103">すべての引数は、関数によって自動的に 0 ～ 360°の範囲に正規化されます。引数に単位を指定しないと、ラジアンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-p103">All of the arguments are automatically normalized between 0 and 360 degrees by the function. If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="bc3b6-133">例 1</span><span class="sxs-lookup"><span data-stu-id="bc3b6-133">Example 1</span></span>

<span data-ttu-id="bc3b6-134">GRAVITY(Angle)</span><span class="sxs-lookup"><span data-stu-id="bc3b6-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="bc3b6-135">180 度の*角度*が 90、270 度の間にある場合を返します。それ以外の場合、0 度を返します。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="bc3b6-136">例 2</span><span class="sxs-lookup"><span data-stu-id="bc3b6-136">Example 2</span></span>

<span data-ttu-id="bc3b6-137">GRAVITY(2)</span><span class="sxs-lookup"><span data-stu-id="bc3b6-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="bc3b6-138">2 ラジアンは 90 ～ 270°の範囲に含まれるため、180°を返します。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bc3b6-139">例 3</span><span class="sxs-lookup"><span data-stu-id="bc3b6-139">Example 3</span></span>

<span data-ttu-id="bc3b6-140">GRAVITY(100 deg, 110 deg, 290 deg)</span><span class="sxs-lookup"><span data-stu-id="bc3b6-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="bc3b6-141">0°を返します。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="bc3b6-142">例 4</span><span class="sxs-lookup"><span data-stu-id="bc3b6-142">Example 4</span></span>

<span data-ttu-id="bc3b6-143">GRAVITY(100 deg, 290 deg, 110 deg)</span><span class="sxs-lookup"><span data-stu-id="bc3b6-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="bc3b6-144">0°を返します。</span><span class="sxs-lookup"><span data-stu-id="bc3b6-144">Returns 0 degrees.</span></span>
  

