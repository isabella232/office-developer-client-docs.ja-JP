---
title: FLOOR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: 数値を 0 (ゼロ) の方向、次の整数、または複数の次のインスタンスに切り上げます。
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439899"
---
# <a name="floor-function"></a><span data-ttu-id="cfa7e-103">FLOOR 関数</span><span class="sxs-lookup"><span data-stu-id="cfa7e-103">FLOOR Function</span></span>

<span data-ttu-id="cfa7e-104">数値を 0 (ゼロ) の方向、次の整数、または_複数_の次のインスタンスに切り上げます。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="cfa7e-105">構文</span><span class="sxs-lookup"><span data-stu-id="cfa7e-105">Syntax</span></span>

<span data-ttu-id="cfa7e-106">床面 (\* **数値** \*, \* \* *multiple* \* \*)</span><span class="sxs-lookup"><span data-stu-id="cfa7e-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cfa7e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cfa7e-107">Parameters</span></span>

|<span data-ttu-id="cfa7e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="cfa7e-108">**Name**</span></span>|<span data-ttu-id="cfa7e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="cfa7e-109">**Required/Optional**</span></span>|<span data-ttu-id="cfa7e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="cfa7e-110">**Data Type**</span></span>|<span data-ttu-id="cfa7e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="cfa7e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cfa7e-112">_number_</span><span class="sxs-lookup"><span data-stu-id="cfa7e-112">_number_</span></span> <br/> |<span data-ttu-id="cfa7e-113">必須</span><span class="sxs-lookup"><span data-stu-id="cfa7e-113">Required</span></span>  <br/> |<span data-ttu-id="cfa7e-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="cfa7e-114">**Number**</span></span> <br/> |<span data-ttu-id="cfa7e-115">切り上げの対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="cfa7e-116">_マルチ_</span><span class="sxs-lookup"><span data-stu-id="cfa7e-116">_multiple_</span></span> <br/> |<span data-ttu-id="cfa7e-117">必須</span><span class="sxs-lookup"><span data-stu-id="cfa7e-117">Required</span></span>  <br/> |<span data-ttu-id="cfa7e-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="cfa7e-118">**Number**</span></span> <br/> |<span data-ttu-id="cfa7e-119">切り上げの対象となる倍数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="cfa7e-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="cfa7e-120">Return value</span></span>

<span data-ttu-id="cfa7e-121">数値</span><span class="sxs-lookup"><span data-stu-id="cfa7e-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cfa7e-122">注釈</span><span class="sxs-lookup"><span data-stu-id="cfa7e-122">Remarks</span></span>

<span data-ttu-id="cfa7e-123">_multiple_が指定されていない場合、数値は0に近づくと次の整数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="cfa7e-124">_数値_と_複数_の値は、同じ記号または #NUM である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="cfa7e-125">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-125">error is returned.</span></span> <span data-ttu-id="cfa7e-126">_数値_、または_複数_の値を値に変換できない場合は、#VALUE します。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="cfa7e-127">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-127">error is returned.</span></span> <span data-ttu-id="cfa7e-128">_数値_または_倍数_が0の場合、結果は0になります。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="cfa7e-129">例 1</span><span class="sxs-lookup"><span data-stu-id="cfa7e-129">Example 1</span></span>

<span data-ttu-id="cfa7e-130">床 (3.7)</span><span class="sxs-lookup"><span data-stu-id="cfa7e-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="cfa7e-131">3 を返します。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="cfa7e-132">例 2</span><span class="sxs-lookup"><span data-stu-id="cfa7e-132">Example 2</span></span>

<span data-ttu-id="cfa7e-133">床面 (-3.7)</span><span class="sxs-lookup"><span data-stu-id="cfa7e-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="cfa7e-134">-3 を返します。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="cfa7e-135">例 3</span><span class="sxs-lookup"><span data-stu-id="cfa7e-135">Example 3</span></span>

<span data-ttu-id="cfa7e-136">床面 (3.7, 0.5)</span><span class="sxs-lookup"><span data-stu-id="cfa7e-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="cfa7e-137">3.5 を返します。</span><span class="sxs-lookup"><span data-stu-id="cfa7e-137">Returns 3.5.</span></span>
  

