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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439969"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="032ba-103">ROUND 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="032ba-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="032ba-104">*numberofdigits*で表される精度に数値を丸めます。</span><span class="sxs-lookup"><span data-stu-id="032ba-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="032ba-105">構文</span><span class="sxs-lookup"><span data-stu-id="032ba-105">Syntax</span></span>

<span data-ttu-id="032ba-106">ROUND (\* **数値** *、* \* *numberofdigits* \* \*)</span><span class="sxs-lookup"><span data-stu-id="032ba-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="032ba-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="032ba-107">Parameters</span></span>

|<span data-ttu-id="032ba-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="032ba-108">**Name**</span></span>|<span data-ttu-id="032ba-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="032ba-109">**Required/Optional**</span></span>|<span data-ttu-id="032ba-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="032ba-110">**Data Type**</span></span>|<span data-ttu-id="032ba-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="032ba-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="032ba-112">_number_</span><span class="sxs-lookup"><span data-stu-id="032ba-112">_number_</span></span> <br/> |<span data-ttu-id="032ba-113">必須</span><span class="sxs-lookup"><span data-stu-id="032ba-113">Required</span></span>  <br/> |<span data-ttu-id="032ba-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="032ba-114">**Number**</span></span> <br/> |<span data-ttu-id="032ba-115">四捨五入の対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="032ba-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="032ba-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="032ba-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="032ba-117">必須</span><span class="sxs-lookup"><span data-stu-id="032ba-117">Required</span></span>  <br/> |<span data-ttu-id="032ba-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="032ba-118">**Number**</span></span> <br/> |<span data-ttu-id="032ba-119">精度の小数点以下桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="032ba-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="032ba-120">注釈</span><span class="sxs-lookup"><span data-stu-id="032ba-120">Remarks</span></span>

<span data-ttu-id="032ba-121">_numberofdigits_が0より大きい場合、_数値_は、 _numberofdigits_の小数点の右側に切り上げられます。</span><span class="sxs-lookup"><span data-stu-id="032ba-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="032ba-122">_numberofdigits_が0の場合、_数値_は整数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="032ba-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="032ba-123">_numberofdigits_が0より小さい場合、_数値_は、 _numberofdigits_の小数点の左に丸められます。</span><span class="sxs-lookup"><span data-stu-id="032ba-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="032ba-124">例 1</span><span class="sxs-lookup"><span data-stu-id="032ba-124">Example 1</span></span>

<span data-ttu-id="032ba-125">ROUND (123.654、2)</span><span class="sxs-lookup"><span data-stu-id="032ba-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="032ba-126">123.65 を返します。</span><span class="sxs-lookup"><span data-stu-id="032ba-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="032ba-127">例 2</span><span class="sxs-lookup"><span data-stu-id="032ba-127">Example 2</span></span>

<span data-ttu-id="032ba-128">ROUND (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="032ba-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="032ba-129">124 を返します。</span><span class="sxs-lookup"><span data-stu-id="032ba-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="032ba-130">例 3</span><span class="sxs-lookup"><span data-stu-id="032ba-130">Example 3</span></span>

<span data-ttu-id="032ba-131">ROUND (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="032ba-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="032ba-132">120 を返します。</span><span class="sxs-lookup"><span data-stu-id="032ba-132">Returns 120.</span></span>
  

