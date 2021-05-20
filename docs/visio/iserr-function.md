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
description: cellreference の値がエラーの種類である場合は TRUE を返します(#N/A を除く)。それ以外の場合は、FALSE を返します。 ISERR 関数は、別のセルを参照する数式で使用されます。
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432108"
---
# <a name="iserr-function"></a><span data-ttu-id="e5c70-104">ISERR 関数</span><span class="sxs-lookup"><span data-stu-id="e5c70-104">ISERR Function</span></span>

<span data-ttu-id="e5c70-105">セル参照の値がエラーの  _種類である場合_ は TRUE を返します(#N/A を除く)。それ以外の場合は、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="e5c70-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="e5c70-106">ISERR 関数は、別のセルを参照する数式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e5c70-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e5c70-107">構文</span><span class="sxs-lookup"><span data-stu-id="e5c70-107">Syntax</span></span>

<span data-ttu-id="e5c70-108">ISERR(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e5c70-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5c70-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e5c70-109">Parameters</span></span>

|<span data-ttu-id="e5c70-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="e5c70-110">**Name**</span></span>|<span data-ttu-id="e5c70-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e5c70-111">**Required/Optional**</span></span>|<span data-ttu-id="e5c70-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e5c70-112">**Data Type**</span></span>|<span data-ttu-id="e5c70-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="e5c70-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5c70-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="e5c70-114">_cellreference_</span></span> <br/> |<span data-ttu-id="e5c70-115">必須</span><span class="sxs-lookup"><span data-stu-id="e5c70-115">Required</span></span>  <br/> |<span data-ttu-id="e5c70-116">**String**</span><span class="sxs-lookup"><span data-stu-id="e5c70-116">**String**</span></span> <br/> |<span data-ttu-id="e5c70-117">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5c70-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="e5c70-118">例 1</span><span class="sxs-lookup"><span data-stu-id="e5c70-118">Example 1</span></span>

|<span data-ttu-id="e5c70-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="e5c70-119">**Cell**</span></span>|<span data-ttu-id="e5c70-120">**式**</span><span class="sxs-lookup"><span data-stu-id="e5c70-120">**Formula**</span></span>|<span data-ttu-id="e5c70-121">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="e5c70-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5c70-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="e5c70-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="e5c70-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="e5c70-123">=NA( )</span></span>  <br/> |<span data-ttu-id="e5c70-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="e5c70-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="e5c70-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="e5c70-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="e5c70-126">=ISERR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="e5c70-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="e5c70-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="e5c70-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="e5c70-p103">ISERR 関数は #N/A! エラーを認識しないため、FALSE を返します。すべてのエラー タイプを検出するには、ISERROR を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5c70-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e5c70-131">例 2</span><span class="sxs-lookup"><span data-stu-id="e5c70-131">Example 2</span></span>

|<span data-ttu-id="e5c70-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="e5c70-132">**Cell**</span></span>|<span data-ttu-id="e5c70-133">**式**</span><span class="sxs-lookup"><span data-stu-id="e5c70-133">**Formula**</span></span>|<span data-ttu-id="e5c70-134">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="e5c70-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5c70-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="e5c70-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="e5c70-136">="House"</span><span class="sxs-lookup"><span data-stu-id="e5c70-136">="House"</span></span>  <br/> |<span data-ttu-id="e5c70-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="e5c70-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="e5c70-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="e5c70-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="e5c70-139">=ISERR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="e5c70-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="e5c70-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="e5c70-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="e5c70-p104">ISERR 関数は #VALUE! エラーを認識するため、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="e5c70-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

