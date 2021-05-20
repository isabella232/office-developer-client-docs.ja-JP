---
title: ROUND 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: 数値を numberofdigits で表される精度に丸します。
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439969"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="e7582-103">ROUND 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="e7582-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="e7582-104">数値を  *numberofdigits*  で表される精度に丸します。</span><span class="sxs-lookup"><span data-stu-id="e7582-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e7582-105">構文</span><span class="sxs-lookup"><span data-stu-id="e7582-105">Syntax</span></span>

<span data-ttu-id="e7582-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e7582-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e7582-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e7582-107">Parameters</span></span>

|<span data-ttu-id="e7582-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="e7582-108">**Name**</span></span>|<span data-ttu-id="e7582-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e7582-109">**Required/Optional**</span></span>|<span data-ttu-id="e7582-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e7582-110">**Data Type**</span></span>|<span data-ttu-id="e7582-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="e7582-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e7582-112">_number_</span><span class="sxs-lookup"><span data-stu-id="e7582-112">_number_</span></span> <br/> |<span data-ttu-id="e7582-113">必須</span><span class="sxs-lookup"><span data-stu-id="e7582-113">Required</span></span>  <br/> |<span data-ttu-id="e7582-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="e7582-114">**Number**</span></span> <br/> |<span data-ttu-id="e7582-115">四捨五入の対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7582-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="e7582-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="e7582-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="e7582-117">必須</span><span class="sxs-lookup"><span data-stu-id="e7582-117">Required</span></span>  <br/> |<span data-ttu-id="e7582-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="e7582-118">**Number**</span></span> <br/> |<span data-ttu-id="e7582-119">精度の小数点以下桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7582-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7582-120">注釈</span><span class="sxs-lookup"><span data-stu-id="e7582-120">Remarks</span></span>

<span data-ttu-id="e7582-121">_numberofdigits が_ 0 より大きい場合、数値は小数点の右側の _numberofdigits_ で四捨五入されます。</span><span class="sxs-lookup"><span data-stu-id="e7582-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="e7582-122">_numberofdigits が_ 0 の場合、_数値は_ 整数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="e7582-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="e7582-123">_numberofdigits が_ 0 より小さい場合、数値は小数点の左側に _numberofdigits_ で四捨五入されます。</span><span class="sxs-lookup"><span data-stu-id="e7582-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e7582-124">例 1</span><span class="sxs-lookup"><span data-stu-id="e7582-124">Example 1</span></span>

<span data-ttu-id="e7582-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="e7582-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="e7582-126">123.65 を返します。</span><span class="sxs-lookup"><span data-stu-id="e7582-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e7582-127">例 2</span><span class="sxs-lookup"><span data-stu-id="e7582-127">Example 2</span></span>

<span data-ttu-id="e7582-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="e7582-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="e7582-129">124 を返します。</span><span class="sxs-lookup"><span data-stu-id="e7582-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e7582-130">例 3</span><span class="sxs-lookup"><span data-stu-id="e7582-130">Example 3</span></span>

<span data-ttu-id="e7582-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="e7582-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="e7582-132">120 を返します。</span><span class="sxs-lookup"><span data-stu-id="e7582-132">Returns 120.</span></span>
  

