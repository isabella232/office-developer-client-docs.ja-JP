---
title: HSL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: 図面のカラー パレットのインデックスを表す値を返します。 色相、彩度および明度のコンポーネントを使用して色を指定します。
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805543"
---
# <a name="hsl-function"></a><span data-ttu-id="3b118-104">HSL 関数</span><span class="sxs-lookup"><span data-stu-id="3b118-104">HSL Function</span></span>

<span data-ttu-id="3b118-105">図面のカラー パレットのインデックスを表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="3b118-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="3b118-106">色相、彩度および明度のコンポーネントを使用して色を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b118-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3b118-107">構文</span><span class="sxs-lookup"><span data-stu-id="3b118-107">Syntax</span></span>

<span data-ttu-id="3b118-108">HSL (* **色合い** *、* **飽和** *、* **明るさ** *)</span><span class="sxs-lookup"><span data-stu-id="3b118-108">HSL(** *hue* **, ** *saturation* **, ** *luminosity* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3b118-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3b118-109">Parameters</span></span>

|<span data-ttu-id="3b118-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="3b118-110">**Name**</span></span>|<span data-ttu-id="3b118-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3b118-111">**Required/Optional**</span></span>|<span data-ttu-id="3b118-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3b118-112">**Data Type**</span></span>|<span data-ttu-id="3b118-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="3b118-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3b118-114">_色合い_</span><span class="sxs-lookup"><span data-stu-id="3b118-114">_hue_</span></span> <br/> |<span data-ttu-id="3b118-115">必須</span><span class="sxs-lookup"><span data-stu-id="3b118-115">Required</span></span>  <br/> |<span data-ttu-id="3b118-116">**番号**</span><span class="sxs-lookup"><span data-stu-id="3b118-116">**Number**</span></span> <br/> |<span data-ttu-id="3b118-117">色の色合いです。0 ～ 239 (0 と 239 を含む) の範囲の数値、またはこの範囲の数値に評価される式を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b118-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="3b118-118">_彩度_</span><span class="sxs-lookup"><span data-stu-id="3b118-118">_saturation_</span></span> <br/> |<span data-ttu-id="3b118-119">必須</span><span class="sxs-lookup"><span data-stu-id="3b118-119">Required</span></span>  <br/> |<span data-ttu-id="3b118-120">**番号**</span><span class="sxs-lookup"><span data-stu-id="3b118-120">**Number**</span></span> <br/> |<span data-ttu-id="3b118-121">色の彩度です。0 ～ 240 (0 と 240 を含む) の範囲の数値、またはこの範囲の数値に評価される式を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b118-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="3b118-122">_明るさ_</span><span class="sxs-lookup"><span data-stu-id="3b118-122">_luminosity_</span></span> <br/> |<span data-ttu-id="3b118-123">必須</span><span class="sxs-lookup"><span data-stu-id="3b118-123">Required</span></span>  <br/> |<span data-ttu-id="3b118-124">**番号**</span><span class="sxs-lookup"><span data-stu-id="3b118-124">**Number**</span></span> <br/> | <span data-ttu-id="3b118-125">色の明度です。0 ～ 240 (0 と 240 を含む) の範囲の数値、またはこの範囲の数値に評価される式を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b118-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3b118-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="3b118-126">Return value</span></span>

<span data-ttu-id="3b118-127">数値</span><span class="sxs-lookup"><span data-stu-id="3b118-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b118-128">注釈</span><span class="sxs-lookup"><span data-stu-id="3b118-128">Remarks</span></span>

<span data-ttu-id="3b118-129">関数によって返される色が現在の図面のカラー パレットにない場合、その色が図面で使用できる色の一覧に追加されます。</span><span class="sxs-lookup"><span data-stu-id="3b118-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="3b118-130">次の表は、標準の色とその色に対する色合い、彩度、明度の値の一覧です。</span><span class="sxs-lookup"><span data-stu-id="3b118-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="3b118-131">**色**</span><span class="sxs-lookup"><span data-stu-id="3b118-131">**Color**</span></span>|<span data-ttu-id="3b118-132">**色合いの値**</span><span class="sxs-lookup"><span data-stu-id="3b118-132">**Hue value**</span></span>|<span data-ttu-id="3b118-133">**彩度の値**</span><span class="sxs-lookup"><span data-stu-id="3b118-133">**Saturation value**</span></span>|<span data-ttu-id="3b118-134">**明度の値**</span><span class="sxs-lookup"><span data-stu-id="3b118-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3b118-135">黒</span><span class="sxs-lookup"><span data-stu-id="3b118-135">Black</span></span>  <br/> |<span data-ttu-id="3b118-136">0</span><span class="sxs-lookup"><span data-stu-id="3b118-136">0</span></span>  <br/> |<span data-ttu-id="3b118-137">0</span><span class="sxs-lookup"><span data-stu-id="3b118-137">0</span></span>  <br/> |<span data-ttu-id="3b118-138">24</span><span class="sxs-lookup"><span data-stu-id="3b118-138">24</span></span>  <br/> |
|<span data-ttu-id="3b118-139">青</span><span class="sxs-lookup"><span data-stu-id="3b118-139">Blue</span></span>  <br/> |<span data-ttu-id="3b118-140">160</span><span class="sxs-lookup"><span data-stu-id="3b118-140">160</span></span>  <br/> |<span data-ttu-id="3b118-141">240</span><span class="sxs-lookup"><span data-stu-id="3b118-141">240</span></span>  <br/> |<span data-ttu-id="3b118-142"> 
120 
</span><span class="sxs-lookup"><span data-stu-id="3b118-142">120</span></span>  <br/> |
|<span data-ttu-id="3b118-143">緑</span><span class="sxs-lookup"><span data-stu-id="3b118-143">Green</span></span>  <br/> |<span data-ttu-id="3b118-144">80</span><span class="sxs-lookup"><span data-stu-id="3b118-144">80</span></span>  <br/> |<span data-ttu-id="3b118-145">240</span><span class="sxs-lookup"><span data-stu-id="3b118-145">240</span></span>  <br/> |<span data-ttu-id="3b118-146"> 
120 
</span><span class="sxs-lookup"><span data-stu-id="3b118-146">120</span></span>  <br/> |
|<span data-ttu-id="3b118-147">シアン</span><span class="sxs-lookup"><span data-stu-id="3b118-147">Cyan</span></span>  <br/> |<span data-ttu-id="3b118-148"> 
120 
</span><span class="sxs-lookup"><span data-stu-id="3b118-148">120</span></span>  <br/> |<span data-ttu-id="3b118-149">240</span><span class="sxs-lookup"><span data-stu-id="3b118-149">240</span></span>  <br/> |<span data-ttu-id="3b118-150"> 
120 
</span><span class="sxs-lookup"><span data-stu-id="3b118-150">120</span></span>  <br/> |
|<span data-ttu-id="3b118-151">赤</span><span class="sxs-lookup"><span data-stu-id="3b118-151">Red</span></span>  <br/> |<span data-ttu-id="3b118-152">0</span><span class="sxs-lookup"><span data-stu-id="3b118-152">0</span></span>  <br/> |<span data-ttu-id="3b118-153">240</span><span class="sxs-lookup"><span data-stu-id="3b118-153">240</span></span>  <br/> |<span data-ttu-id="3b118-154"> 
120 
</span><span class="sxs-lookup"><span data-stu-id="3b118-154">120</span></span>  <br/> |
|<span data-ttu-id="3b118-155">マゼンタ</span><span class="sxs-lookup"><span data-stu-id="3b118-155">Magenta</span></span>  <br/> |<span data-ttu-id="3b118-156"> 
200 
</span><span class="sxs-lookup"><span data-stu-id="3b118-156">200</span></span>  <br/> |<span data-ttu-id="3b118-157">240</span><span class="sxs-lookup"><span data-stu-id="3b118-157">240</span></span>  <br/> |<span data-ttu-id="3b118-158"> 
120 
</span><span class="sxs-lookup"><span data-stu-id="3b118-158">120</span></span>  <br/> |
|<span data-ttu-id="3b118-159">黄</span><span class="sxs-lookup"><span data-stu-id="3b118-159">Yellow</span></span>  <br/> |<span data-ttu-id="3b118-160">40</span><span class="sxs-lookup"><span data-stu-id="3b118-160">40</span></span>  <br/> |<span data-ttu-id="3b118-161">240</span><span class="sxs-lookup"><span data-stu-id="3b118-161">240</span></span>  <br/> |<span data-ttu-id="3b118-162"> 
120 
</span><span class="sxs-lookup"><span data-stu-id="3b118-162">120</span></span>  <br/> |
|<span data-ttu-id="3b118-163">白</span><span class="sxs-lookup"><span data-stu-id="3b118-163">White</span></span>  <br/> |<span data-ttu-id="3b118-164">0</span><span class="sxs-lookup"><span data-stu-id="3b118-164">0</span></span>  <br/> |<span data-ttu-id="3b118-165">0</span><span class="sxs-lookup"><span data-stu-id="3b118-165">0</span></span>  <br/> |<span data-ttu-id="3b118-166">240</span><span class="sxs-lookup"><span data-stu-id="3b118-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="3b118-167">例 1</span><span class="sxs-lookup"><span data-stu-id="3b118-167">Example 1</span></span>

<span data-ttu-id="3b118-168">HSL(160,240,120)</span><span class="sxs-lookup"><span data-stu-id="3b118-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="3b118-169">青色に対するインデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="3b118-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3b118-170">例 2</span><span class="sxs-lookup"><span data-stu-id="3b118-170">Example 2</span></span>

<span data-ttu-id="3b118-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span><span class="sxs-lookup"><span data-stu-id="3b118-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="3b118-172">前景の塗りつぶしの色に対して明度を高くしたときの、色のインデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="3b118-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

