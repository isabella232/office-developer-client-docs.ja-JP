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
description: 文字列が同じかどうかを判断します。 値が同じ場合に TRUE を返します false の場合は、します。
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806567"
---
# <a name="strsame-function"></a><span data-ttu-id="f59ab-104">STRSAME 関数</span><span class="sxs-lookup"><span data-stu-id="f59ab-104">STRSAME Function</span></span>

<span data-ttu-id="f59ab-105">文字列が同じかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-105">Determines whether strings are the same.</span></span> <span data-ttu-id="f59ab-106">値が同じ場合に TRUE を返します false の場合は、します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f59ab-107">構文</span><span class="sxs-lookup"><span data-stu-id="f59ab-107">Syntax</span></span>

<span data-ttu-id="f59ab-108">STRSAME ("* * *string1* * *「,」* **文字列 2* * *」、* * *ignoreCase* * *)</span><span class="sxs-lookup"><span data-stu-id="f59ab-108">STRSAME (" ** *string1* ** ", " ** *string2* ** ", ** *ignoreCase* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f59ab-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="f59ab-109">Parameters</span></span>

|<span data-ttu-id="f59ab-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="f59ab-110">**Name**</span></span>|<span data-ttu-id="f59ab-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f59ab-111">**Required/Optional**</span></span>|<span data-ttu-id="f59ab-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f59ab-112">**Data Type**</span></span>|<span data-ttu-id="f59ab-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="f59ab-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f59ab-114">_文字列 1_</span><span class="sxs-lookup"><span data-stu-id="f59ab-114">_string1_</span></span> <br/> |<span data-ttu-id="f59ab-115">必須</span><span class="sxs-lookup"><span data-stu-id="f59ab-115">Required</span></span>  <br/> |<span data-ttu-id="f59ab-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="f59ab-116">**String**</span></span> <br/> |<span data-ttu-id="f59ab-117">比較する最初の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="f59ab-118">_文字列 2_</span><span class="sxs-lookup"><span data-stu-id="f59ab-118">_string2_</span></span> <br/> |<span data-ttu-id="f59ab-119">必須</span><span class="sxs-lookup"><span data-stu-id="f59ab-119">Required</span></span>  <br/> |<span data-ttu-id="f59ab-120">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="f59ab-120">**String**</span></span> <br/> |<span data-ttu-id="f59ab-121">比較する 2 番目の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="f59ab-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="f59ab-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="f59ab-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="f59ab-123">Optional</span></span>  <br/> |<span data-ttu-id="f59ab-124">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="f59ab-124">**Boolean**</span></span> <br/> |<span data-ttu-id="f59ab-p103">大文字/小文字を区別しない場合は TRUE を、大文字/小文字を区別する場合は FALSE を指定します。既定値は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="f59ab-p103">TRUE to ignore the case and FALSE to compare the case. The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f59ab-127">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f59ab-127">Return value</span></span>

<span data-ttu-id="f59ab-128">ブール型 (Boolean)</span><span class="sxs-lookup"><span data-stu-id="f59ab-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f59ab-129">注釈</span><span class="sxs-lookup"><span data-stu-id="f59ab-129">Remarks</span></span>

<span data-ttu-id="f59ab-130">マルチバイト文字列の比較、または特定のロケールに関する文字の規則を使用した比較を実行する場合は、STRSAMEEX 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="f59ab-131">例 1</span><span class="sxs-lookup"><span data-stu-id="f59ab-131">Example 1</span></span>

<span data-ttu-id="f59ab-132">STRSAME("cat","dog")</span><span class="sxs-lookup"><span data-stu-id="f59ab-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="f59ab-133">FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f59ab-134">例 2</span><span class="sxs-lookup"><span data-stu-id="f59ab-134">Example 2</span></span>

<span data-ttu-id="f59ab-135">STRSAME("cat","cat")</span><span class="sxs-lookup"><span data-stu-id="f59ab-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="f59ab-136">TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f59ab-137">例 3</span><span class="sxs-lookup"><span data-stu-id="f59ab-137">Example 3</span></span>

<span data-ttu-id="f59ab-138">STRSAME("cat","cat", TRUE)</span><span class="sxs-lookup"><span data-stu-id="f59ab-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="f59ab-139">TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="f59ab-140">例 4</span><span class="sxs-lookup"><span data-stu-id="f59ab-140">Example 4</span></span>

<span data-ttu-id="f59ab-141">STRSAME("cat","CAT")</span><span class="sxs-lookup"><span data-stu-id="f59ab-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="f59ab-142">FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="f59ab-143">例 5</span><span class="sxs-lookup"><span data-stu-id="f59ab-143">Example 5</span></span>

<span data-ttu-id="f59ab-144">STRSAME("cat","CAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="f59ab-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="f59ab-145">TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="f59ab-146">例 6</span><span class="sxs-lookup"><span data-stu-id="f59ab-146">Example 6</span></span>

<span data-ttu-id="f59ab-147">STRSAME("cät,"CAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="f59ab-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="f59ab-148">FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="f59ab-149">例 7</span><span class="sxs-lookup"><span data-stu-id="f59ab-149">Example 7</span></span>

<span data-ttu-id="f59ab-150">STRSAME("cät,"CÄT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="f59ab-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="f59ab-151">TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="f59ab-151">Returns TRUE.</span></span>
  

