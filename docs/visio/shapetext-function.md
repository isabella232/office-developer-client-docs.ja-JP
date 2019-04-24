---
title: SHAPETEXT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: 図形からテキストを取得します。
ms.openlocfilehash: bb9b1fbe5900cd051828ed6c7ff07546567c1b23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349113"
---
# <a name="shapetext-function"></a><span data-ttu-id="abb54-103">SHAPETEXT 関数</span><span class="sxs-lookup"><span data-stu-id="abb54-103">SHAPETEXT Function</span></span>

<span data-ttu-id="abb54-104">図形からテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="abb54-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="abb54-105">構文</span><span class="sxs-lookup"><span data-stu-id="abb54-105">Syntax</span></span>

<span data-ttu-id="abb54-106">図形のテキスト (\* \**図形)* テキスト \* \* \* \* *[, flag]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="abb54-106">SHAPETEXT (\*\* *shapename!TheText* \*\* \*\* *[,flag]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="abb54-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="abb54-107">Parameters</span></span>

|<span data-ttu-id="abb54-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="abb54-108">**Name**</span></span>|<span data-ttu-id="abb54-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="abb54-109">**Required/Optional**</span></span>|<span data-ttu-id="abb54-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="abb54-110">**Data Type**</span></span>|<span data-ttu-id="abb54-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="abb54-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="abb54-112">_shapename![thetext]_</span><span class="sxs-lookup"><span data-stu-id="abb54-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="abb54-113">必須</span><span class="sxs-lookup"><span data-stu-id="abb54-113">Required</span></span>  <br/> ||<span data-ttu-id="abb54-114">ターゲットとなる図形の [TheText] セルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="abb54-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="abb54-115">_Shapename!_</span><span class="sxs-lookup"><span data-stu-id="abb54-115">_Shapename!_</span></span> <span data-ttu-id="abb54-116">は、テキストを取得する図形の名前です。</span><span class="sxs-lookup"><span data-stu-id="abb54-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="abb54-117">_flag_</span><span class="sxs-lookup"><span data-stu-id="abb54-117">_flag_</span></span> <br/> |<span data-ttu-id="abb54-118">省略可能</span><span class="sxs-lookup"><span data-stu-id="abb54-118">Optional</span></span>  <br/> |<span data-ttu-id="abb54-119">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="abb54-119">**Numeric**</span></span> <br/> |<span data-ttu-id="abb54-120">テキストの書式を示すビットを指定します。</span><span class="sxs-lookup"><span data-stu-id="abb54-120">A bit that specifies the format of the text.</span></span> <span data-ttu-id="abb54-121">既定のフラグ (0) は、図形に表示されるとおりにテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="abb54-121">The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="abb54-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="abb54-122">Return value</span></span>

<span data-ttu-id="abb54-123">文字列</span><span class="sxs-lookup"><span data-stu-id="abb54-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="abb54-124">注釈</span><span class="sxs-lookup"><span data-stu-id="abb54-124">Remarks</span></span>

<span data-ttu-id="abb54-125">SHAPETEXT 関数では、次のフラグを任意に組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="abb54-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="abb54-126">**Flag**</span><span class="sxs-lookup"><span data-stu-id="abb54-126">**Flag**</span></span>|<span data-ttu-id="abb54-127">**説明**</span><span class="sxs-lookup"><span data-stu-id="abb54-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abb54-128">.0</span><span class="sxs-lookup"><span data-stu-id="abb54-128">0</span></span>  <br/> |<span data-ttu-id="abb54-129">図形に表示されているとおりにテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="abb54-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="abb54-130">1-d</span><span class="sxs-lookup"><span data-stu-id="abb54-130">1</span></span>  <br/> |<span data-ttu-id="abb54-131">任意のハイフンを含みます。</span><span class="sxs-lookup"><span data-stu-id="abb54-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="abb54-132">pbm-2</span><span class="sxs-lookup"><span data-stu-id="abb54-132">2</span></span>  <br/> |<span data-ttu-id="abb54-133">フィールドの拡張テキストは除外されます。</span><span class="sxs-lookup"><span data-stu-id="abb54-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="abb54-134">2/4</span><span class="sxs-lookup"><span data-stu-id="abb54-134">4</span></span>  <br/> |<span data-ttu-id="abb54-135">タブを単一のスペースに変換します。</span><span class="sxs-lookup"><span data-stu-id="abb54-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="abb54-136">~</span><span class="sxs-lookup"><span data-stu-id="abb54-136">8</span></span>  <br/> |<span data-ttu-id="abb54-137">タブを複数のスペースに変換します。</span><span class="sxs-lookup"><span data-stu-id="abb54-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="abb54-138">16</span><span class="sxs-lookup"><span data-stu-id="abb54-138">16</span></span>  <br/> |<span data-ttu-id="abb54-139">改行文字と行送りをスペースに変換します。</span><span class="sxs-lookup"><span data-stu-id="abb54-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="abb54-140">32</span><span class="sxs-lookup"><span data-stu-id="abb54-140">32</span></span>  <br/> |<span data-ttu-id="abb54-141">印刷用の引用符を通常の引用符に変換します。</span><span class="sxs-lookup"><span data-stu-id="abb54-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="abb54-142">64</span><span class="sxs-lookup"><span data-stu-id="abb54-142">64</span></span>  <br/> |<span data-ttu-id="abb54-143">隣接した余白を単一のスペースに変換します。</span><span class="sxs-lookup"><span data-stu-id="abb54-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="abb54-144">例 1</span><span class="sxs-lookup"><span data-stu-id="abb54-144">Example 1</span></span>

<span data-ttu-id="abb54-145">図形のテキスト (中)</span><span class="sxs-lookup"><span data-stu-id="abb54-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="abb54-146">図形に表示されているとおりに、sheetN という図形のテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="abb54-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="abb54-147">例 2</span><span class="sxs-lookup"><span data-stu-id="abb54-147">Example 2</span></span>

<span data-ttu-id="abb54-148">図形のテキスト (テキスト)</span><span class="sxs-lookup"><span data-stu-id="abb54-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="abb54-149">図形に表示されているとおりに、現在の図形のテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="abb54-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="abb54-150">例 3</span><span class="sxs-lookup"><span data-stu-id="abb54-150">Example 3</span></span>

<span data-ttu-id="abb54-151">SHAPETEXT(theText, 84)</span><span class="sxs-lookup"><span data-stu-id="abb54-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="abb54-p103">現在の図形のテキストを返します。隣接した余白から単一のスペースへの変換 (64)、改行文字と行送りのスペースへの変換 (16)、およびタブの単一のスペースへの変換 (4) も行います。これらのフラグの合計は 84 です。</span><span class="sxs-lookup"><span data-stu-id="abb54-p103">Returns the text of the current shape. It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4). The sum of these flags is 84.</span></span>
  

