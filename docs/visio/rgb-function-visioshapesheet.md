---
title: RGB 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: 図面のカラー パレットのインデックスを表す値を返します。 範囲 0 ~ 255 の範囲の数字をそれぞれ、赤、緑、および青コンポーネントを使用して色を指定します。
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806233"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="dc88a-104">RGB 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="dc88a-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="dc88a-105">図面のカラー パレットのインデックスを表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="dc88a-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="dc88a-106">範囲 0 ~ 255 の範囲の数字をそれぞれ、赤、緑、および青コンポーネントを使用して色を指定します。</span><span class="sxs-lookup"><span data-stu-id="dc88a-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dc88a-107">構文</span><span class="sxs-lookup"><span data-stu-id="dc88a-107">Syntax</span></span>

<span data-ttu-id="dc88a-108">RGB (* **赤** *、* **緑** *、* **ブルー* * *)</span><span class="sxs-lookup"><span data-stu-id="dc88a-108">RGB(** *red* **, ** *green* **, ** *blue* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dc88a-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="dc88a-109">Parameters</span></span>

|<span data-ttu-id="dc88a-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="dc88a-110">**Name**</span></span>|<span data-ttu-id="dc88a-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="dc88a-111">**Required/Optional**</span></span>|<span data-ttu-id="dc88a-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="dc88a-112">**Data Type**</span></span>|<span data-ttu-id="dc88a-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="dc88a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dc88a-114">_red_</span><span class="sxs-lookup"><span data-stu-id="dc88a-114">_red_</span></span> <br/> |<span data-ttu-id="dc88a-115">必須</span><span class="sxs-lookup"><span data-stu-id="dc88a-115">Required</span></span>  <br/> |<span data-ttu-id="dc88a-116">**番号**</span><span class="sxs-lookup"><span data-stu-id="dc88a-116">**Number**</span></span> <br/> |<span data-ttu-id="dc88a-117">赤のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc88a-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="dc88a-118">_green_</span><span class="sxs-lookup"><span data-stu-id="dc88a-118">_green_</span></span> <br/> |<span data-ttu-id="dc88a-119">必須</span><span class="sxs-lookup"><span data-stu-id="dc88a-119">Required</span></span>  <br/> |<span data-ttu-id="dc88a-120">**番号**</span><span class="sxs-lookup"><span data-stu-id="dc88a-120">**Number**</span></span> <br/> |<span data-ttu-id="dc88a-121">緑のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc88a-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="dc88a-122">_blue_</span><span class="sxs-lookup"><span data-stu-id="dc88a-122">_blue_</span></span> <br/> |<span data-ttu-id="dc88a-123">必須</span><span class="sxs-lookup"><span data-stu-id="dc88a-123">Required</span></span>  <br/> |<span data-ttu-id="dc88a-124">**番号**</span><span class="sxs-lookup"><span data-stu-id="dc88a-124">**Nmber**</span></span> <br/> |<span data-ttu-id="dc88a-125">青のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc88a-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dc88a-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="dc88a-126">Return value</span></span>

<span data-ttu-id="dc88a-127">数値</span><span class="sxs-lookup"><span data-stu-id="dc88a-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc88a-128">注釈</span><span class="sxs-lookup"><span data-stu-id="dc88a-128">Remarks</span></span>

<span data-ttu-id="dc88a-129">関数が返す色が現在の図面のカラー パレットにない場合、その色がパレットに追加されます。</span><span class="sxs-lookup"><span data-stu-id="dc88a-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="dc88a-130">次の表は、標準色とその色に対する赤、緑、青コンポーネントの値の一覧です。</span><span class="sxs-lookup"><span data-stu-id="dc88a-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="dc88a-131">**色**</span><span class="sxs-lookup"><span data-stu-id="dc88a-131">**Color**</span></span>|<span data-ttu-id="dc88a-132">**赤の値**</span><span class="sxs-lookup"><span data-stu-id="dc88a-132">**Red value**</span></span>|<span data-ttu-id="dc88a-133">**緑の値**</span><span class="sxs-lookup"><span data-stu-id="dc88a-133">**Green value**</span></span>|<span data-ttu-id="dc88a-134">**青の値**</span><span class="sxs-lookup"><span data-stu-id="dc88a-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dc88a-135">黒</span><span class="sxs-lookup"><span data-stu-id="dc88a-135">Black</span></span>  <br/> |<span data-ttu-id="dc88a-136">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-136">0</span></span>  <br/> |<span data-ttu-id="dc88a-137">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-137">0</span></span>  <br/> |<span data-ttu-id="dc88a-138">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-138">0</span></span>  <br/> |
|<span data-ttu-id="dc88a-139">青</span><span class="sxs-lookup"><span data-stu-id="dc88a-139">Blue</span></span>  <br/> |<span data-ttu-id="dc88a-140">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-140">0</span></span>  <br/> |<span data-ttu-id="dc88a-141">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-141">0</span></span>  <br/> |<span data-ttu-id="dc88a-142">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-142">255</span></span>  <br/> |
|<span data-ttu-id="dc88a-143">緑</span><span class="sxs-lookup"><span data-stu-id="dc88a-143">Green</span></span>  <br/> |<span data-ttu-id="dc88a-144">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-144">0</span></span>  <br/> |<span data-ttu-id="dc88a-145">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-145">255</span></span>  <br/> |<span data-ttu-id="dc88a-146">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-146">0</span></span>  <br/> |
|<span data-ttu-id="dc88a-147">シアン</span><span class="sxs-lookup"><span data-stu-id="dc88a-147">Cyan</span></span>  <br/> |<span data-ttu-id="dc88a-148">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-148">0</span></span>  <br/> |<span data-ttu-id="dc88a-149">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-149">255</span></span>  <br/> |<span data-ttu-id="dc88a-150">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-150">255</span></span>  <br/> |
|<span data-ttu-id="dc88a-151">赤</span><span class="sxs-lookup"><span data-stu-id="dc88a-151">Red</span></span>  <br/> |<span data-ttu-id="dc88a-152">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-152">255</span></span>  <br/> |<span data-ttu-id="dc88a-153">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-153">0</span></span>  <br/> |<span data-ttu-id="dc88a-154">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-154">0</span></span>  <br/> |
|<span data-ttu-id="dc88a-155">マゼンダ</span><span class="sxs-lookup"><span data-stu-id="dc88a-155">Magenta</span></span>  <br/> |<span data-ttu-id="dc88a-156">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-156">255</span></span>  <br/> |<span data-ttu-id="dc88a-157">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-157">0</span></span>  <br/> |<span data-ttu-id="dc88a-158">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-158">255</span></span>  <br/> |
|<span data-ttu-id="dc88a-159">黄</span><span class="sxs-lookup"><span data-stu-id="dc88a-159">Yellow</span></span>  <br/> |<span data-ttu-id="dc88a-160">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-160">255</span></span>  <br/> |<span data-ttu-id="dc88a-161">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-161">255</span></span>  <br/> |<span data-ttu-id="dc88a-162">0</span><span class="sxs-lookup"><span data-stu-id="dc88a-162">0</span></span>  <br/> |
|<span data-ttu-id="dc88a-163">白</span><span class="sxs-lookup"><span data-stu-id="dc88a-163">White</span></span>  <br/> |<span data-ttu-id="dc88a-164">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-164">255</span></span>  <br/> |<span data-ttu-id="dc88a-165">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-165">255</span></span>  <br/> |<span data-ttu-id="dc88a-166">255</span><span class="sxs-lookup"><span data-stu-id="dc88a-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="dc88a-167">例 1</span><span class="sxs-lookup"><span data-stu-id="dc88a-167">Example 1</span></span>

<span data-ttu-id="dc88a-168">RGB(0,0,255)</span><span class="sxs-lookup"><span data-stu-id="dc88a-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="dc88a-169">青色に対するインデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="dc88a-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dc88a-170">例 2</span><span class="sxs-lookup"><span data-stu-id="dc88a-170">Example 2</span></span>

<span data-ttu-id="dc88a-171">RGB (赤 (Sheet.1!FillForegnd)、120, 0)</span><span class="sxs-lookup"><span data-stu-id="dc88a-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="dc88a-172">Sheet.1 の前景の塗りつぶし色に適用されている赤コンポーネントを使用して、色のインデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="dc88a-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

