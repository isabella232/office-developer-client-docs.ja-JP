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
description: numberofdigits で表される精度に数値を丸めます。
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315576"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="d35ca-103">ROUND 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d35ca-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d35ca-104">*numberofdigits*で表される精度に数値を丸めます。</span><span class="sxs-lookup"><span data-stu-id="d35ca-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d35ca-105">構文</span><span class="sxs-lookup"><span data-stu-id="d35ca-105">Syntax</span></span>

<span data-ttu-id="d35ca-106">ROUND (\* **数値** *、* \* *numberofdigits* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d35ca-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d35ca-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d35ca-107">Parameters</span></span>

|<span data-ttu-id="d35ca-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d35ca-108">**Name**</span></span>|<span data-ttu-id="d35ca-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d35ca-109">**Required/Optional**</span></span>|<span data-ttu-id="d35ca-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d35ca-110">**Data Type**</span></span>|<span data-ttu-id="d35ca-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d35ca-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d35ca-112">_number_</span><span class="sxs-lookup"><span data-stu-id="d35ca-112">_number_</span></span> <br/> |<span data-ttu-id="d35ca-113">必須</span><span class="sxs-lookup"><span data-stu-id="d35ca-113">Required</span></span>  <br/> |<span data-ttu-id="d35ca-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="d35ca-114">**Number**</span></span> <br/> |<span data-ttu-id="d35ca-115">四捨五入の対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d35ca-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="d35ca-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="d35ca-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="d35ca-117">必須</span><span class="sxs-lookup"><span data-stu-id="d35ca-117">Required</span></span>  <br/> |<span data-ttu-id="d35ca-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="d35ca-118">**Number**</span></span> <br/> |<span data-ttu-id="d35ca-119">精度の小数点以下桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d35ca-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d35ca-120">解説</span><span class="sxs-lookup"><span data-stu-id="d35ca-120">Remarks</span></span>

<span data-ttu-id="d35ca-121">_numberofdigits_が0より大きい場合、_数値_は、 _numberofdigits_の小数点の右側に切り上げられます。</span><span class="sxs-lookup"><span data-stu-id="d35ca-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="d35ca-122">_numberofdigits_が0の場合、_数値_は整数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="d35ca-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="d35ca-123">_numberofdigits_が0より小さい場合、_数値_は、 _numberofdigits_の小数点の左に丸められます。</span><span class="sxs-lookup"><span data-stu-id="d35ca-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d35ca-124">例 1</span><span class="sxs-lookup"><span data-stu-id="d35ca-124">Example 1</span></span>

<span data-ttu-id="d35ca-125">ROUND (123.654、2)</span><span class="sxs-lookup"><span data-stu-id="d35ca-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="d35ca-126">123.65 を返します。</span><span class="sxs-lookup"><span data-stu-id="d35ca-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d35ca-127">例 2</span><span class="sxs-lookup"><span data-stu-id="d35ca-127">Example 2</span></span>

<span data-ttu-id="d35ca-128">ROUND (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="d35ca-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="d35ca-129">124 を返します。</span><span class="sxs-lookup"><span data-stu-id="d35ca-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d35ca-130">例 3</span><span class="sxs-lookup"><span data-stu-id="d35ca-130">Example 3</span></span>

<span data-ttu-id="d35ca-131">ROUND (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="d35ca-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="d35ca-132">120 を返します。</span><span class="sxs-lookup"><span data-stu-id="d35ca-132">Returns 120.</span></span>
  

