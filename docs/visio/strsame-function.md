---
title: STRSAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: 文字列が同じかどうかを判断します。 同じである場合は TRUE を返し、そうでない場合は FALSE を返します。
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329842"
---
# <a name="strsame-function"></a><span data-ttu-id="0ca08-104">STRSAME 関数</span><span class="sxs-lookup"><span data-stu-id="0ca08-104">STRSAME Function</span></span>

<span data-ttu-id="0ca08-105">文字列が同じかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-105">Determines whether strings are the same.</span></span> <span data-ttu-id="0ca08-106">同じである場合は TRUE を返し、そうでない場合は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0ca08-107">構文</span><span class="sxs-lookup"><span data-stu-id="0ca08-107">Syntax</span></span>

<span data-ttu-id="0ca08-108">strsame ("\* \* *string1* \* *", "* \* *string2* \* \*", \* \* *ignoreCase* \* \*)</span><span class="sxs-lookup"><span data-stu-id="0ca08-108">STRSAME (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *ignoreCase* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0ca08-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0ca08-109">Parameters</span></span>

|<span data-ttu-id="0ca08-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="0ca08-110">**Name**</span></span>|<span data-ttu-id="0ca08-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0ca08-111">**Required/Optional**</span></span>|<span data-ttu-id="0ca08-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0ca08-112">**Data Type**</span></span>|<span data-ttu-id="0ca08-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="0ca08-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0ca08-114">_string1_</span><span class="sxs-lookup"><span data-stu-id="0ca08-114">_string1_</span></span> <br/> |<span data-ttu-id="0ca08-115">必須</span><span class="sxs-lookup"><span data-stu-id="0ca08-115">Required</span></span>  <br/> |<span data-ttu-id="0ca08-116">**String**</span><span class="sxs-lookup"><span data-stu-id="0ca08-116">**String**</span></span> <br/> |<span data-ttu-id="0ca08-117">比較する最初の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="0ca08-118">_string2_</span><span class="sxs-lookup"><span data-stu-id="0ca08-118">_string2_</span></span> <br/> |<span data-ttu-id="0ca08-119">必須</span><span class="sxs-lookup"><span data-stu-id="0ca08-119">Required</span></span>  <br/> |<span data-ttu-id="0ca08-120">**String**</span><span class="sxs-lookup"><span data-stu-id="0ca08-120">**String**</span></span> <br/> |<span data-ttu-id="0ca08-121">比較する 2 番目の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="0ca08-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="0ca08-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="0ca08-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="0ca08-123">Optional</span></span>  <br/> |<span data-ttu-id="0ca08-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0ca08-124">**Boolean**</span></span> <br/> |<span data-ttu-id="0ca08-125">大文字/小文字を区別しない場合は TRUE を、大文字/小文字を区別する場合は FALSE を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-125">TRUE to ignore the case and FALSE to compare the case.</span></span> <span data-ttu-id="0ca08-126">既定値は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="0ca08-126">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0ca08-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="0ca08-127">Return value</span></span>

<span data-ttu-id="0ca08-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="0ca08-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ca08-129">解説</span><span class="sxs-lookup"><span data-stu-id="0ca08-129">Remarks</span></span>

<span data-ttu-id="0ca08-130">マルチバイト文字列の比較、または特定のロケールに関する文字の規則を使用した比較を実行する場合は、STRSAMEEX 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="0ca08-131">例 1</span><span class="sxs-lookup"><span data-stu-id="0ca08-131">Example 1</span></span>

<span data-ttu-id="0ca08-132">strsame ("cat", "dog")</span><span class="sxs-lookup"><span data-stu-id="0ca08-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="0ca08-133">FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0ca08-134">例 2</span><span class="sxs-lookup"><span data-stu-id="0ca08-134">Example 2</span></span>

<span data-ttu-id="0ca08-135">strsame ("cat", "cat")</span><span class="sxs-lookup"><span data-stu-id="0ca08-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="0ca08-136">TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0ca08-137">例 3</span><span class="sxs-lookup"><span data-stu-id="0ca08-137">Example 3</span></span>

<span data-ttu-id="0ca08-138">STRSAME("cat","cat", TRUE)</span><span class="sxs-lookup"><span data-stu-id="0ca08-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="0ca08-139">TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="0ca08-140">例 4</span><span class="sxs-lookup"><span data-stu-id="0ca08-140">Example 4</span></span>

<span data-ttu-id="0ca08-141">strsame ("cat", "cat")</span><span class="sxs-lookup"><span data-stu-id="0ca08-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="0ca08-142">FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="0ca08-143">例 5</span><span class="sxs-lookup"><span data-stu-id="0ca08-143">Example 5</span></span>

<span data-ttu-id="0ca08-144">STRSAME("cat","CAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="0ca08-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="0ca08-145">TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="0ca08-146">例 6</span><span class="sxs-lookup"><span data-stu-id="0ca08-146">Example 6</span></span>

<span data-ttu-id="0ca08-147">STRSAME("cät,"CAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="0ca08-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="0ca08-148">FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="0ca08-149">例 7</span><span class="sxs-lookup"><span data-stu-id="0ca08-149">Example 7</span></span>

<span data-ttu-id="0ca08-150">STRSAME("cät,"CÄT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="0ca08-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="0ca08-151">TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="0ca08-151">Returns TRUE.</span></span>
  

