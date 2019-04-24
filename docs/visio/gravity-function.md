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
description: 指定した図形の回転のテキストブロックの正確な角度を計算し、テキストが逆さまになるのを防ぎます。
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360187"
---
# <a name="gravity-function"></a><span data-ttu-id="18fd2-103">GRAVITY 関数</span><span class="sxs-lookup"><span data-stu-id="18fd2-103">GRAVITY Function</span></span>

<span data-ttu-id="18fd2-104">指定した図形の回転のテキストブロックの正確な角度を計算し、テキストが逆さまになるのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="18fd2-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="18fd2-105">構文</span><span class="sxs-lookup"><span data-stu-id="18fd2-105">Syntax</span></span>

<span data-ttu-id="18fd2-106">重力 (\* **角度** *、[* \**制限 1* \* *]、[* \* *limit2* \* \*])</span><span class="sxs-lookup"><span data-stu-id="18fd2-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="18fd2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="18fd2-107">Parameters</span></span>

|<span data-ttu-id="18fd2-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="18fd2-108">**Name**</span></span>|<span data-ttu-id="18fd2-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="18fd2-109">**Required/Optional**</span></span>|<span data-ttu-id="18fd2-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="18fd2-110">**Data Type**</span></span>|<span data-ttu-id="18fd2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="18fd2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="18fd2-112">_直交_</span><span class="sxs-lookup"><span data-stu-id="18fd2-112">_angle_</span></span> <br/> |<span data-ttu-id="18fd2-113">必須</span><span class="sxs-lookup"><span data-stu-id="18fd2-113">Required</span></span>  <br/> |<span data-ttu-id="18fd2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="18fd2-114">**String**</span></span> <br/> | <span data-ttu-id="18fd2-115">図形の角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="18fd2-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="18fd2-116">_制限1_</span><span class="sxs-lookup"><span data-stu-id="18fd2-116">_limit1_</span></span> <br/> |<span data-ttu-id="18fd2-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="18fd2-117">Optional</span></span>  <br/> |<span data-ttu-id="18fd2-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="18fd2-118">**String**</span></span> <br/> |<span data-ttu-id="18fd2-119">回転の最初の制限角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="18fd2-119">First limit of rotation.</span></span> <span data-ttu-id="18fd2-120">既定の制限角度は 90°です。</span><span class="sxs-lookup"><span data-stu-id="18fd2-120">Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="18fd2-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="18fd2-121">_limit2_</span></span> <br/> |<span data-ttu-id="18fd2-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="18fd2-122">Optional</span></span>  <br/> |<span data-ttu-id="18fd2-123">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="18fd2-123">**String**</span></span> <br/> |<span data-ttu-id="18fd2-124">回転の 2 番目の制限角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="18fd2-124">Second limit of rotation.</span></span> <span data-ttu-id="18fd2-125">既定の制限角度は 270°です。</span><span class="sxs-lookup"><span data-stu-id="18fd2-125">Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="18fd2-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="18fd2-126">Return value</span></span>

<span data-ttu-id="18fd2-127">文字列</span><span class="sxs-lookup"><span data-stu-id="18fd2-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18fd2-128">注釈</span><span class="sxs-lookup"><span data-stu-id="18fd2-128">Remarks</span></span>

<span data-ttu-id="18fd2-129">通常、GRAVITY 関数は [TxtAngle] セルで使用します。</span><span class="sxs-lookup"><span data-stu-id="18fd2-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="18fd2-130">_角度_が_制限 1_および_limit2_で指定された値の間にある場合、返される値は180°になります。それ以外の場合、返される値は0°です。</span><span class="sxs-lookup"><span data-stu-id="18fd2-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="18fd2-131">すべての引数は、関数によって自動的に 0 ～ 360°の範囲に正規化されます。</span><span class="sxs-lookup"><span data-stu-id="18fd2-131">All of the arguments are automatically normalized between 0 and 360 degrees by the function.</span></span> <span data-ttu-id="18fd2-132">引数に単位を指定しないと、ラジアンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="18fd2-132">If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="18fd2-133">例 1</span><span class="sxs-lookup"><span data-stu-id="18fd2-133">Example 1</span></span>

<span data-ttu-id="18fd2-134">重力 (角度)</span><span class="sxs-lookup"><span data-stu-id="18fd2-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="18fd2-135">*角度*が 90 ~ 270 度の場合、180°を返します。それ以外の場合は0°を返します。</span><span class="sxs-lookup"><span data-stu-id="18fd2-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="18fd2-136">例 2</span><span class="sxs-lookup"><span data-stu-id="18fd2-136">Example 2</span></span>

<span data-ttu-id="18fd2-137">重力 (2)</span><span class="sxs-lookup"><span data-stu-id="18fd2-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="18fd2-138">2 ラジアンは 90 ～ 270°の範囲に含まれるため、180°を返します。</span><span class="sxs-lookup"><span data-stu-id="18fd2-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="18fd2-139">例 3</span><span class="sxs-lookup"><span data-stu-id="18fd2-139">Example 3</span></span>

<span data-ttu-id="18fd2-140">GRAVITY(100 deg, 110 deg, 290 deg)</span><span class="sxs-lookup"><span data-stu-id="18fd2-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="18fd2-141">0°を返します。</span><span class="sxs-lookup"><span data-stu-id="18fd2-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="18fd2-142">例 4</span><span class="sxs-lookup"><span data-stu-id="18fd2-142">Example 4</span></span>

<span data-ttu-id="18fd2-143">GRAVITY(100 deg, 290 deg, 110 deg)</span><span class="sxs-lookup"><span data-stu-id="18fd2-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="18fd2-144">0°を返します。</span><span class="sxs-lookup"><span data-stu-id="18fd2-144">Returns 0 degrees.</span></span>
  

