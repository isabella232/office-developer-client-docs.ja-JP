---
title: ISERR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'cellreference の値が #N/a 以外のエラーの種類の場合は TRUE を返します。それ以外の場合は、FALSE を返します。 iserr 関数は、別のセルを参照する数式で使用されます。'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297250"
---
# <a name="iserr-function"></a><span data-ttu-id="3b1c8-104">ISERR 関数</span><span class="sxs-lookup"><span data-stu-id="3b1c8-104">ISERR Function</span></span>

<span data-ttu-id="3b1c8-105">_cellreference_の値が #N/a 以外のエラーの種類の場合は TRUE を返します。それ以外の場合は、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="3b1c8-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="3b1c8-106">iserr 関数は、別のセルを参照する数式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="3b1c8-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3b1c8-107">構文</span><span class="sxs-lookup"><span data-stu-id="3b1c8-107">Syntax</span></span>

<span data-ttu-id="3b1c8-108">iserr (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3b1c8-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3b1c8-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3b1c8-109">Parameters</span></span>

|<span data-ttu-id="3b1c8-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-110">**Name**</span></span>|<span data-ttu-id="3b1c8-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-111">**Required/Optional**</span></span>|<span data-ttu-id="3b1c8-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-112">**Data Type**</span></span>|<span data-ttu-id="3b1c8-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3b1c8-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="3b1c8-114">_cellreference_</span></span> <br/> |<span data-ttu-id="3b1c8-115">必須</span><span class="sxs-lookup"><span data-stu-id="3b1c8-115">Required</span></span>  <br/> |<span data-ttu-id="3b1c8-116">**String**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-116">**String**</span></span> <br/> |<span data-ttu-id="3b1c8-117">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b1c8-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="3b1c8-118">例 1</span><span class="sxs-lookup"><span data-stu-id="3b1c8-118">Example 1</span></span>

|<span data-ttu-id="3b1c8-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-119">**Cell**</span></span>|<span data-ttu-id="3b1c8-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-120">**Formula**</span></span>|<span data-ttu-id="3b1c8-121">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b1c8-122">最初の A1</span><span class="sxs-lookup"><span data-stu-id="3b1c8-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="3b1c8-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="3b1c8-123">=NA( )</span></span>  <br/> |<span data-ttu-id="3b1c8-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="3b1c8-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="3b1c8-125">最初の B1</span><span class="sxs-lookup"><span data-stu-id="3b1c8-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="3b1c8-126">= iserr (A1)</span><span class="sxs-lookup"><span data-stu-id="3b1c8-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="3b1c8-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="3b1c8-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="3b1c8-p103">ISERR 関数は #N/A! エラーを認識しないため、FALSE を返します。すべてのエラー タイプを検出するには、ISERROR を使用します。</span><span class="sxs-lookup"><span data-stu-id="3b1c8-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3b1c8-131">例 2</span><span class="sxs-lookup"><span data-stu-id="3b1c8-131">Example 2</span></span>

|<span data-ttu-id="3b1c8-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-132">**Cell**</span></span>|<span data-ttu-id="3b1c8-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-133">**Formula**</span></span>|<span data-ttu-id="3b1c8-134">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="3b1c8-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b1c8-135">最初の X1</span><span class="sxs-lookup"><span data-stu-id="3b1c8-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="3b1c8-136">= "House"</span><span class="sxs-lookup"><span data-stu-id="3b1c8-136">="House"</span></span>  <br/> |<span data-ttu-id="3b1c8-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="3b1c8-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="3b1c8-138">最初の A1</span><span class="sxs-lookup"><span data-stu-id="3b1c8-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="3b1c8-139">= iserr (最初の X1)</span><span class="sxs-lookup"><span data-stu-id="3b1c8-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="3b1c8-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="3b1c8-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="3b1c8-p104">ISERR 関数は #VALUE! エラーを認識するため、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="3b1c8-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

