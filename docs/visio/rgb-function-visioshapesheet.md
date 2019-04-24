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
description: ドキュメントのカラーパレット内のインデックスを表す値を返します。 赤、緑、青のコンポーネントで色を指定します。各要素は、0 ~ 255 の範囲の数値、またはそのような数値に評価される式です。
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326741"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="30d75-104">RGB 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="30d75-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="30d75-105">ドキュメントのカラーパレット内のインデックスを表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="30d75-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="30d75-106">赤、緑、青のコンポーネントで色を指定します。各要素は、0 ~ 255 の範囲の数値、またはそのような数値に評価される式です。</span><span class="sxs-lookup"><span data-stu-id="30d75-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="30d75-107">構文</span><span class="sxs-lookup"><span data-stu-id="30d75-107">Syntax</span></span>

<span data-ttu-id="30d75-108">RGB (\* **赤** *、* \* *green* \* *、* \* *blue* \* \*)</span><span class="sxs-lookup"><span data-stu-id="30d75-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="30d75-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="30d75-109">Parameters</span></span>

|<span data-ttu-id="30d75-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="30d75-110">**Name**</span></span>|<span data-ttu-id="30d75-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="30d75-111">**Required/Optional**</span></span>|<span data-ttu-id="30d75-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="30d75-112">**Data Type**</span></span>|<span data-ttu-id="30d75-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="30d75-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="30d75-114">_red_</span><span class="sxs-lookup"><span data-stu-id="30d75-114">_red_</span></span> <br/> |<span data-ttu-id="30d75-115">必須</span><span class="sxs-lookup"><span data-stu-id="30d75-115">Required</span></span>  <br/> |<span data-ttu-id="30d75-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="30d75-116">**Number**</span></span> <br/> |<span data-ttu-id="30d75-117">赤のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="30d75-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="30d75-118">_green_</span><span class="sxs-lookup"><span data-stu-id="30d75-118">_green_</span></span> <br/> |<span data-ttu-id="30d75-119">必須</span><span class="sxs-lookup"><span data-stu-id="30d75-119">Required</span></span>  <br/> |<span data-ttu-id="30d75-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="30d75-120">**Number**</span></span> <br/> |<span data-ttu-id="30d75-121">緑のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="30d75-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="30d75-122">_blue_</span><span class="sxs-lookup"><span data-stu-id="30d75-122">_blue_</span></span> <br/> |<span data-ttu-id="30d75-123">必須</span><span class="sxs-lookup"><span data-stu-id="30d75-123">Required</span></span>  <br/> |<span data-ttu-id="30d75-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="30d75-124">**Nmber**</span></span> <br/> |<span data-ttu-id="30d75-125">青のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="30d75-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="30d75-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="30d75-126">Return value</span></span>

<span data-ttu-id="30d75-127">番号</span><span class="sxs-lookup"><span data-stu-id="30d75-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30d75-128">解説</span><span class="sxs-lookup"><span data-stu-id="30d75-128">Remarks</span></span>

<span data-ttu-id="30d75-129">関数が返す色が現在の図面のカラー パレットにない場合、その色がパレットに追加されます。</span><span class="sxs-lookup"><span data-stu-id="30d75-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="30d75-130">次の表は、標準色とその色に対する赤、緑、青コンポーネントの値の一覧です。</span><span class="sxs-lookup"><span data-stu-id="30d75-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="30d75-131">**色**</span><span class="sxs-lookup"><span data-stu-id="30d75-131">**Color**</span></span>|<span data-ttu-id="30d75-132">**赤の値**</span><span class="sxs-lookup"><span data-stu-id="30d75-132">**Red value**</span></span>|<span data-ttu-id="30d75-133">**緑の値**</span><span class="sxs-lookup"><span data-stu-id="30d75-133">**Green value**</span></span>|<span data-ttu-id="30d75-134">**青の値**</span><span class="sxs-lookup"><span data-stu-id="30d75-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="30d75-135">黒</span><span class="sxs-lookup"><span data-stu-id="30d75-135">Black</span></span>  <br/> |<span data-ttu-id="30d75-136">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-136">0</span></span>  <br/> |<span data-ttu-id="30d75-137">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-137">0</span></span>  <br/> |<span data-ttu-id="30d75-138">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-138">0</span></span>  <br/> |
|<span data-ttu-id="30d75-139">青</span><span class="sxs-lookup"><span data-stu-id="30d75-139">Blue</span></span>  <br/> |<span data-ttu-id="30d75-140">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-140">0</span></span>  <br/> |<span data-ttu-id="30d75-141">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-141">0</span></span>  <br/> |<span data-ttu-id="30d75-142">255</span><span class="sxs-lookup"><span data-stu-id="30d75-142">255</span></span>  <br/> |
|<span data-ttu-id="30d75-143">緑</span><span class="sxs-lookup"><span data-stu-id="30d75-143">Green</span></span>  <br/> |<span data-ttu-id="30d75-144">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-144">0</span></span>  <br/> |<span data-ttu-id="30d75-145">255</span><span class="sxs-lookup"><span data-stu-id="30d75-145">255</span></span>  <br/> |<span data-ttu-id="30d75-146">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-146">0</span></span>  <br/> |
|<span data-ttu-id="30d75-147">シアン</span><span class="sxs-lookup"><span data-stu-id="30d75-147">Cyan</span></span>  <br/> |<span data-ttu-id="30d75-148">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-148">0</span></span>  <br/> |<span data-ttu-id="30d75-149">255</span><span class="sxs-lookup"><span data-stu-id="30d75-149">255</span></span>  <br/> |<span data-ttu-id="30d75-150">255</span><span class="sxs-lookup"><span data-stu-id="30d75-150">255</span></span>  <br/> |
|<span data-ttu-id="30d75-151">赤</span><span class="sxs-lookup"><span data-stu-id="30d75-151">Red</span></span>  <br/> |<span data-ttu-id="30d75-152">255</span><span class="sxs-lookup"><span data-stu-id="30d75-152">255</span></span>  <br/> |<span data-ttu-id="30d75-153">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-153">0</span></span>  <br/> |<span data-ttu-id="30d75-154">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-154">0</span></span>  <br/> |
|<span data-ttu-id="30d75-155">マゼンダ</span><span class="sxs-lookup"><span data-stu-id="30d75-155">Magenta</span></span>  <br/> |<span data-ttu-id="30d75-156">255</span><span class="sxs-lookup"><span data-stu-id="30d75-156">255</span></span>  <br/> |<span data-ttu-id="30d75-157">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-157">0</span></span>  <br/> |<span data-ttu-id="30d75-158">255</span><span class="sxs-lookup"><span data-stu-id="30d75-158">255</span></span>  <br/> |
|<span data-ttu-id="30d75-159">黄色</span><span class="sxs-lookup"><span data-stu-id="30d75-159">Yellow</span></span>  <br/> |<span data-ttu-id="30d75-160">255</span><span class="sxs-lookup"><span data-stu-id="30d75-160">255</span></span>  <br/> |<span data-ttu-id="30d75-161">255</span><span class="sxs-lookup"><span data-stu-id="30d75-161">255</span></span>  <br/> |<span data-ttu-id="30d75-162">.0</span><span class="sxs-lookup"><span data-stu-id="30d75-162">0</span></span>  <br/> |
|<span data-ttu-id="30d75-163">白</span><span class="sxs-lookup"><span data-stu-id="30d75-163">White</span></span>  <br/> |<span data-ttu-id="30d75-164">255</span><span class="sxs-lookup"><span data-stu-id="30d75-164">255</span></span>  <br/> |<span data-ttu-id="30d75-165">255</span><span class="sxs-lookup"><span data-stu-id="30d75-165">255</span></span>  <br/> |<span data-ttu-id="30d75-166">255</span><span class="sxs-lookup"><span data-stu-id="30d75-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="30d75-167">例 1</span><span class="sxs-lookup"><span data-stu-id="30d75-167">Example 1</span></span>

<span data-ttu-id="30d75-168">RGB (0、0255)</span><span class="sxs-lookup"><span data-stu-id="30d75-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="30d75-169">青色に対するインデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="30d75-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="30d75-170">例 2</span><span class="sxs-lookup"><span data-stu-id="30d75-170">Example 2</span></span>

<span data-ttu-id="30d75-171">RGB (赤 (Sheet. 1![fillforegnd])、120、0)</span><span class="sxs-lookup"><span data-stu-id="30d75-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="30d75-172">Sheet.1 の前景の塗りつぶし色に適用されている赤コンポーネントを使用して、色のインデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="30d75-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

