---
title: TRUNC 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: 指定した桁数に切り詰められた数値を返します。
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426500"
---
# <a name="trunc-function"></a><span data-ttu-id="7f4d9-103">TRUNC 関数</span><span class="sxs-lookup"><span data-stu-id="7f4d9-103">TRUNC Function</span></span>

<span data-ttu-id="7f4d9-104">指定した桁数に切り詰められた数値を返します。</span><span class="sxs-lookup"><span data-stu-id="7f4d9-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7f4d9-105">構文</span><span class="sxs-lookup"><span data-stu-id="7f4d9-105">Syntax</span></span>

<span data-ttu-id="7f4d9-106">TRUNC (\* \* *number* \* \*, \* \* *numberofdigits* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7f4d9-106">TRUNC(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7f4d9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7f4d9-107">Parameters</span></span>

|<span data-ttu-id="7f4d9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="7f4d9-108">**Name**</span></span>|<span data-ttu-id="7f4d9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="7f4d9-109">**Required/Optional**</span></span>|<span data-ttu-id="7f4d9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="7f4d9-110">**Data Type**</span></span>|<span data-ttu-id="7f4d9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="7f4d9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7f4d9-112">_number_</span><span class="sxs-lookup"><span data-stu-id="7f4d9-112">_number_</span></span> <br/> |<span data-ttu-id="7f4d9-113">必須</span><span class="sxs-lookup"><span data-stu-id="7f4d9-113">Required</span></span>  <br/> |<span data-ttu-id="7f4d9-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="7f4d9-114">**Numeric**</span></span> <br/> |<span data-ttu-id="7f4d9-115">切り捨ての対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f4d9-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="7f4d9-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="7f4d9-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="7f4d9-117">必須</span><span class="sxs-lookup"><span data-stu-id="7f4d9-117">Required</span></span>  <br/> |<span data-ttu-id="7f4d9-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="7f4d9-118">**Numeric**</span></span> <br/> |<span data-ttu-id="7f4d9-119">_数値_を切り捨てる桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f4d9-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7f4d9-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="7f4d9-120">Return value</span></span>

<span data-ttu-id="7f4d9-121">数値型</span><span class="sxs-lookup"><span data-stu-id="7f4d9-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f4d9-122">注釈</span><span class="sxs-lookup"><span data-stu-id="7f4d9-122">Remarks</span></span>

<span data-ttu-id="7f4d9-123">_numberofdigits_が0より大きい場合、引数_number_は、その小数点の右側にある_numberofdigits_に切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="7f4d9-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="7f4d9-124">_numberofdigits_が0の場合、_数値_は整数に切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="7f4d9-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="7f4d9-125">_numberofdigits_が0より小さい場合、_数値_は、その小数点の左側の_numberofdigits_に切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="7f4d9-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7f4d9-126">例 1</span><span class="sxs-lookup"><span data-stu-id="7f4d9-126">Example 1</span></span>

<span data-ttu-id="7f4d9-127">TRUNC (123.654, 2)</span><span class="sxs-lookup"><span data-stu-id="7f4d9-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="7f4d9-128">123.65 を返します。</span><span class="sxs-lookup"><span data-stu-id="7f4d9-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7f4d9-129">例 2</span><span class="sxs-lookup"><span data-stu-id="7f4d9-129">Example 2</span></span>

<span data-ttu-id="7f4d9-130">TRUNC (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="7f4d9-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="7f4d9-131">123 を返します。</span><span class="sxs-lookup"><span data-stu-id="7f4d9-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7f4d9-132">例 3</span><span class="sxs-lookup"><span data-stu-id="7f4d9-132">Example 3</span></span>

<span data-ttu-id="7f4d9-133">TRUNC (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="7f4d9-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="7f4d9-134">120 を返します。</span><span class="sxs-lookup"><span data-stu-id="7f4d9-134">Returns 120.</span></span>
  

