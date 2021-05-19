---
title: SIGN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: 数値の符号を表す値を返します。
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420655"
---
# <a name="sign-function"></a><span data-ttu-id="b313d-103">SIGN 関数</span><span class="sxs-lookup"><span data-stu-id="b313d-103">SIGN Function</span></span>

<span data-ttu-id="b313d-104">数値の符号を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="b313d-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b313d-105">構文</span><span class="sxs-lookup"><span data-stu-id="b313d-105">Syntax</span></span>

<span data-ttu-id="b313d-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span><span class="sxs-lookup"><span data-stu-id="b313d-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b313d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b313d-107">Parameters</span></span>

|<span data-ttu-id="b313d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="b313d-108">**Name**</span></span>|<span data-ttu-id="b313d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="b313d-109">**Required/Optional**</span></span>|<span data-ttu-id="b313d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="b313d-110">**Data Type**</span></span>|<span data-ttu-id="b313d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="b313d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b313d-112">_number_</span><span class="sxs-lookup"><span data-stu-id="b313d-112">_number_</span></span> <br/> |<span data-ttu-id="b313d-113">必須</span><span class="sxs-lookup"><span data-stu-id="b313d-113">Required</span></span>  <br/> |<span data-ttu-id="b313d-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="b313d-114">**Numeric**</span></span> <br/> | <span data-ttu-id="b313d-115">符号を確認する数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b313d-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="b313d-116">_ファズ_</span><span class="sxs-lookup"><span data-stu-id="b313d-116">_fuzz_</span></span> <br/> |<span data-ttu-id="b313d-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="b313d-117">Optional</span></span>  <br/> |<span data-ttu-id="b313d-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="b313d-118">**Numeric**</span></span> <br/> |<span data-ttu-id="b313d-119">指定した数値と 0 との誤差を指定します。数値と 0 の差がこの誤差以内である場合に、数値は 0 として扱われます。</span><span class="sxs-lookup"><span data-stu-id="b313d-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b313d-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="b313d-120">Return value</span></span>

<span data-ttu-id="b313d-121">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="b313d-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b313d-122">注釈</span><span class="sxs-lookup"><span data-stu-id="b313d-122">Remarks</span></span>

<span data-ttu-id="b313d-123">SIGN 関数は、数値が正の場合は 1、数値が 0 の場合は 0、数値が負の場合は -1 _を返_ します。</span><span class="sxs-lookup"><span data-stu-id="b313d-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="b313d-124">あいまいな値  _を指定すると_ 、計算がほぼ 0 の場合に浮動小数点の丸めエラーを回避できます。</span><span class="sxs-lookup"><span data-stu-id="b313d-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="b313d-125">ファジー値を指定しない場合、Visio 1E-9 (0.0000000001) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b313d-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="b313d-126">図面の縮尺を変更したり、正確な比較を行う場合は、異なる値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b313d-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b313d-127">例 1</span><span class="sxs-lookup"><span data-stu-id="b313d-127">Example 1</span></span>

<span data-ttu-id="b313d-128">SIGN(-5)</span><span class="sxs-lookup"><span data-stu-id="b313d-128">SIGN(-5)</span></span>
  
<span data-ttu-id="b313d-129">-1 を返します。</span><span class="sxs-lookup"><span data-stu-id="b313d-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b313d-130">例 2</span><span class="sxs-lookup"><span data-stu-id="b313d-130">Example 2</span></span>

<span data-ttu-id="b313d-131">SIGN(0)</span><span class="sxs-lookup"><span data-stu-id="b313d-131">SIGN(0)</span></span>
  
<span data-ttu-id="b313d-132">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="b313d-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b313d-133">例 3</span><span class="sxs-lookup"><span data-stu-id="b313d-133">Example 3</span></span>

<span data-ttu-id="b313d-134">SIGN(0.000000000001)</span><span class="sxs-lookup"><span data-stu-id="b313d-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="b313d-135">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="b313d-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="b313d-136">例 4</span><span class="sxs-lookup"><span data-stu-id="b313d-136">Example 4</span></span>

<span data-ttu-id="b313d-137">SIGN(0.000000000001,0)</span><span class="sxs-lookup"><span data-stu-id="b313d-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="b313d-138">1 を返します。</span><span class="sxs-lookup"><span data-stu-id="b313d-138">Returns 1.</span></span>
  

