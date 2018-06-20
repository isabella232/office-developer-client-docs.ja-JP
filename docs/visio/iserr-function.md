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
description: Cellreference の値が、エラーの種類である場合に TRUE を返します以外の有効です。それ以外の場合、FALSE を返します。 ISERR 関数は、別のセルを参照する数式で使用されます。
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805606"
---
# <a name="iserr-function"></a><span data-ttu-id="4516e-104">ISERR 関数</span><span class="sxs-lookup"><span data-stu-id="4516e-104">ISERR Function</span></span>

<span data-ttu-id="4516e-105">_Cellreference_の値が、エラーの種類である場合は TRUE を返します以外の有効です。それ以外の場合、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="4516e-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="4516e-106">ISERR 関数は、別のセルを参照する数式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="4516e-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4516e-107">構文</span><span class="sxs-lookup"><span data-stu-id="4516e-107">Syntax</span></span>

<span data-ttu-id="4516e-108">ISERR (* * *cellreference* * *)</span><span class="sxs-lookup"><span data-stu-id="4516e-108">ISERR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4516e-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="4516e-109">Parameters</span></span>

|<span data-ttu-id="4516e-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="4516e-110">**Name**</span></span>|<span data-ttu-id="4516e-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="4516e-111">**Required/Optional**</span></span>|<span data-ttu-id="4516e-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="4516e-112">**Data Type**</span></span>|<span data-ttu-id="4516e-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="4516e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4516e-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="4516e-114">_cellreference_</span></span> <br/> |<span data-ttu-id="4516e-115">必須</span><span class="sxs-lookup"><span data-stu-id="4516e-115">Required</span></span>  <br/> |<span data-ttu-id="4516e-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4516e-116">**String**</span></span> <br/> |<span data-ttu-id="4516e-117">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="4516e-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="4516e-118">例 1</span><span class="sxs-lookup"><span data-stu-id="4516e-118">Example 1</span></span>

|<span data-ttu-id="4516e-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4516e-119">**Cell**</span></span>|<span data-ttu-id="4516e-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="4516e-120">**Formula**</span></span>|<span data-ttu-id="4516e-121">**返される値**</span><span class="sxs-lookup"><span data-stu-id="4516e-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4516e-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="4516e-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="4516e-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="4516e-123">=NA( )</span></span>  <br/> |<span data-ttu-id="4516e-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="4516e-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="4516e-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="4516e-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="4516e-126">=ISERR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="4516e-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="4516e-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="4516e-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="4516e-p103">ISERR 関数は #N/A! エラーを認識しないため、FALSE を返します。すべてのエラー タイプを検出するには、ISERROR を使用します。</span><span class="sxs-lookup"><span data-stu-id="4516e-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4516e-131">例 2</span><span class="sxs-lookup"><span data-stu-id="4516e-131">Example 2</span></span>

|<span data-ttu-id="4516e-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4516e-132">**Cell**</span></span>|<span data-ttu-id="4516e-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="4516e-133">**Formula**</span></span>|<span data-ttu-id="4516e-134">**返される値**</span><span class="sxs-lookup"><span data-stu-id="4516e-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4516e-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="4516e-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="4516e-136">="House"</span><span class="sxs-lookup"><span data-stu-id="4516e-136">="House"</span></span>  <br/> |<span data-ttu-id="4516e-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="4516e-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="4516e-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="4516e-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="4516e-139">=ISERR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="4516e-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="4516e-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="4516e-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="4516e-p104">ISERR 関数は #VALUE! エラーを認識するため、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="4516e-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

