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
description: 指定された桁数に切り捨てられる数を返します。
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806688"
---
# <a name="trunc-function"></a><span data-ttu-id="8b922-103">TRUNC 関数</span><span class="sxs-lookup"><span data-stu-id="8b922-103">TRUNC Function</span></span>

<span data-ttu-id="8b922-104">指定された桁数に切り捨てられる数を返します。</span><span class="sxs-lookup"><span data-stu-id="8b922-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8b922-105">構文</span><span class="sxs-lookup"><span data-stu-id="8b922-105">Syntax</span></span>

<span data-ttu-id="8b922-106">TRUNC (* **番号** *、* * *numberofdigits* * *)</span><span class="sxs-lookup"><span data-stu-id="8b922-106">TRUNC(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8b922-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b922-107">Parameters</span></span>

|<span data-ttu-id="8b922-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="8b922-108">**Name**</span></span>|<span data-ttu-id="8b922-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="8b922-109">**Required/Optional**</span></span>|<span data-ttu-id="8b922-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="8b922-110">**Data Type**</span></span>|<span data-ttu-id="8b922-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="8b922-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8b922-112">_number_</span><span class="sxs-lookup"><span data-stu-id="8b922-112">_number_</span></span> <br/> |<span data-ttu-id="8b922-113">必須</span><span class="sxs-lookup"><span data-stu-id="8b922-113">Required</span></span>  <br/> |<span data-ttu-id="8b922-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="8b922-114">**Numeric**</span></span> <br/> |<span data-ttu-id="8b922-115">切り捨ての対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8b922-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="8b922-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="8b922-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="8b922-117">必須</span><span class="sxs-lookup"><span data-stu-id="8b922-117">Required</span></span>  <br/> |<span data-ttu-id="8b922-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="8b922-118">**Numeric**</span></span> <br/> |<span data-ttu-id="8b922-119">切り捨てる_数値_を桁の数です。</span><span class="sxs-lookup"><span data-stu-id="8b922-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8b922-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="8b922-120">Return value</span></span>

<span data-ttu-id="8b922-121">数値</span><span class="sxs-lookup"><span data-stu-id="8b922-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8b922-122">注釈</span><span class="sxs-lookup"><span data-stu-id="8b922-122">Remarks</span></span>

<span data-ttu-id="8b922-123">_Numberofdigits_が 0 より大きい場合は、_数値_は小数点の右側に_numberofdigits_に切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="8b922-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="8b922-124">_Numberofdigits_が 0 の場合は、_数値_が整数に切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="8b922-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="8b922-125">_Numberofdigits_が 0 より小さい場合は、_数値_は小数点の左側に_numberofdigits_に切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="8b922-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="8b922-126">例 1</span><span class="sxs-lookup"><span data-stu-id="8b922-126">Example 1</span></span>

<span data-ttu-id="8b922-127">TRUNC(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="8b922-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="8b922-128">123.65 を返します。</span><span class="sxs-lookup"><span data-stu-id="8b922-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8b922-129">例 2</span><span class="sxs-lookup"><span data-stu-id="8b922-129">Example 2</span></span>

<span data-ttu-id="8b922-130">TRUNC(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="8b922-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="8b922-131">123 を返します。</span><span class="sxs-lookup"><span data-stu-id="8b922-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8b922-132">例 3</span><span class="sxs-lookup"><span data-stu-id="8b922-132">Example 3</span></span>

<span data-ttu-id="8b922-133">TRUNC(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="8b922-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="8b922-134">120 を返します。</span><span class="sxs-lookup"><span data-stu-id="8b922-134">Returns 120.</span></span>
  

