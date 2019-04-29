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
# <a name="sign-function"></a><span data-ttu-id="df2e8-103">SIGN 関数</span><span class="sxs-lookup"><span data-stu-id="df2e8-103">SIGN Function</span></span>

<span data-ttu-id="df2e8-104">数値の符号を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="df2e8-105">構文</span><span class="sxs-lookup"><span data-stu-id="df2e8-105">Syntax</span></span>

<span data-ttu-id="df2e8-106">SIGN (\* \* *number* \* \*, \* \**ファジー* \* \*)</span><span class="sxs-lookup"><span data-stu-id="df2e8-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="df2e8-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="df2e8-107">Parameters</span></span>

|<span data-ttu-id="df2e8-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="df2e8-108">**Name**</span></span>|<span data-ttu-id="df2e8-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="df2e8-109">**Required/Optional**</span></span>|<span data-ttu-id="df2e8-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="df2e8-110">**Data Type**</span></span>|<span data-ttu-id="df2e8-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="df2e8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df2e8-112">_number_</span><span class="sxs-lookup"><span data-stu-id="df2e8-112">_number_</span></span> <br/> |<span data-ttu-id="df2e8-113">必須</span><span class="sxs-lookup"><span data-stu-id="df2e8-113">Required</span></span>  <br/> |<span data-ttu-id="df2e8-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="df2e8-114">**Numeric**</span></span> <br/> | <span data-ttu-id="df2e8-115">符号を確認する数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="df2e8-116">_ファジー_</span><span class="sxs-lookup"><span data-stu-id="df2e8-116">_fuzz_</span></span> <br/> |<span data-ttu-id="df2e8-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="df2e8-117">Optional</span></span>  <br/> |<span data-ttu-id="df2e8-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="df2e8-118">**Numeric**</span></span> <br/> |<span data-ttu-id="df2e8-119">指定した数値と 0 との誤差を指定します。数値と 0 の差がこの誤差以内である場合に、数値は 0 として扱われます。</span><span class="sxs-lookup"><span data-stu-id="df2e8-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="df2e8-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="df2e8-120">Return value</span></span>

<span data-ttu-id="df2e8-121">数値</span><span class="sxs-lookup"><span data-stu-id="df2e8-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df2e8-122">注釈</span><span class="sxs-lookup"><span data-stu-id="df2e8-122">Remarks</span></span>

<span data-ttu-id="df2e8-123">SIGN 関数は、 _number_が正の場合は1、 __ 数値が0の場合は0、_数値_が負の場合は-1 を返します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="df2e8-124">_ファジー_値を指定すると、計算がほぼゼロの場合に浮動小数点 roundoff エラーを回避できます。</span><span class="sxs-lookup"><span data-stu-id="df2e8-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="df2e8-125">_ファジー_値を指定しない場合、Visio は 1e-9 (0.000000001) を使用します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="df2e8-126">図面の縮尺を変更したり、正確な比較を行う場合は、異なる値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="df2e8-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="df2e8-127">例 1</span><span class="sxs-lookup"><span data-stu-id="df2e8-127">Example 1</span></span>

<span data-ttu-id="df2e8-128">符号 (-5)</span><span class="sxs-lookup"><span data-stu-id="df2e8-128">SIGN(-5)</span></span>
  
<span data-ttu-id="df2e8-129">-1 を返します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="df2e8-130">例 2</span><span class="sxs-lookup"><span data-stu-id="df2e8-130">Example 2</span></span>

<span data-ttu-id="df2e8-131">符号 (0)</span><span class="sxs-lookup"><span data-stu-id="df2e8-131">SIGN(0)</span></span>
  
<span data-ttu-id="df2e8-132">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="df2e8-133">例 3</span><span class="sxs-lookup"><span data-stu-id="df2e8-133">Example 3</span></span>

<span data-ttu-id="df2e8-134">記号 (0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="df2e8-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="df2e8-135">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="df2e8-136">例 4</span><span class="sxs-lookup"><span data-stu-id="df2e8-136">Example 4</span></span>

<span data-ttu-id="df2e8-137">符号 (0.00000000001, 0)</span><span class="sxs-lookup"><span data-stu-id="df2e8-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="df2e8-138">1 を返します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-138">Returns 1.</span></span>
  

