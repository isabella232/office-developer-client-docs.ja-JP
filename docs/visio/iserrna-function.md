---
title: ISERRNA 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'cellreference の値がエラーの種類である場合は TRUE を返します #N/a! (使用できません)、それ以外の場合は、FALSE を返します。 ISERRNA 関数は、別のセルを参照する数式で使用されます。'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357261"
---
# <a name="iserrna-function"></a><span data-ttu-id="1eeef-105">ISERRNA 関数</span><span class="sxs-lookup"><span data-stu-id="1eeef-105">ISERRNA Function</span></span>

<span data-ttu-id="1eeef-106">_cellreference_の値がエラーの種類である場合は TRUE を返します #N/a!</span><span class="sxs-lookup"><span data-stu-id="1eeef-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="1eeef-107">(使用できません)、それ以外の場合は、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="1eeef-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="1eeef-108">ISERRNA 関数は、別のセルを参照する数式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="1eeef-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1eeef-109">構文</span><span class="sxs-lookup"><span data-stu-id="1eeef-109">Syntax</span></span>

<span data-ttu-id="1eeef-110">ISERRNA (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="1eeef-110">ISERRNA(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1eeef-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1eeef-111">Parameters</span></span>

|<span data-ttu-id="1eeef-112">**名前**</span><span class="sxs-lookup"><span data-stu-id="1eeef-112">**Name**</span></span>|<span data-ttu-id="1eeef-113">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="1eeef-113">**Required/Optional**</span></span>|<span data-ttu-id="1eeef-114">**データ型**</span><span class="sxs-lookup"><span data-stu-id="1eeef-114">**Data Type**</span></span>|<span data-ttu-id="1eeef-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="1eeef-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1eeef-116">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="1eeef-116">_cellreference_</span></span> <br/> |<span data-ttu-id="1eeef-117">必須</span><span class="sxs-lookup"><span data-stu-id="1eeef-117">Required</span></span>  <br/> |<span data-ttu-id="1eeef-118">**String**</span><span class="sxs-lookup"><span data-stu-id="1eeef-118">**String**</span></span> <br/> |<span data-ttu-id="1eeef-119">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="1eeef-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="1eeef-120">例 1</span><span class="sxs-lookup"><span data-stu-id="1eeef-120">Example 1</span></span>

|<span data-ttu-id="1eeef-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1eeef-121">**Cell**</span></span>|<span data-ttu-id="1eeef-122">**Formula**</span><span class="sxs-lookup"><span data-stu-id="1eeef-122">**Formula**</span></span>|<span data-ttu-id="1eeef-123">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="1eeef-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1eeef-124">最初の A1</span><span class="sxs-lookup"><span data-stu-id="1eeef-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="1eeef-125">="5 + 3"</span><span class="sxs-lookup"><span data-stu-id="1eeef-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="1eeef-126">~</span><span class="sxs-lookup"><span data-stu-id="1eeef-126">"8"</span></span>  <br/> |
|<span data-ttu-id="1eeef-127">最初の B1</span><span class="sxs-lookup"><span data-stu-id="1eeef-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="1eeef-128">= ISERRNA (A1)</span><span class="sxs-lookup"><span data-stu-id="1eeef-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="1eeef-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="1eeef-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="1eeef-130">戻り値が有効であるため、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="1eeef-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1eeef-131">例 2</span><span class="sxs-lookup"><span data-stu-id="1eeef-131">Example 2</span></span>

|<span data-ttu-id="1eeef-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1eeef-132">**Cell**</span></span>|<span data-ttu-id="1eeef-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="1eeef-133">**Formula**</span></span>|<span data-ttu-id="1eeef-134">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="1eeef-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1eeef-135">最初の A1</span><span class="sxs-lookup"><span data-stu-id="1eeef-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="1eeef-136">=NA( )</span><span class="sxs-lookup"><span data-stu-id="1eeef-136">=NA( )</span></span>  <br/> |<span data-ttu-id="1eeef-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="1eeef-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="1eeef-138">最初の B1</span><span class="sxs-lookup"><span data-stu-id="1eeef-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="1eeef-139">= ISERRNA (A1)</span><span class="sxs-lookup"><span data-stu-id="1eeef-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="1eeef-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="1eeef-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="1eeef-141">戻り値がエラー タイプ #N/A! であるため、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="1eeef-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

