---
title: CEILING 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: 数値を 0 (ゼロ) から次の複数のインスタンスに切り上げします。 multiple を指定しない場合、数値は 0 から次の整数に丸められます。
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404128"
---
# <a name="ceiling-function"></a><span data-ttu-id="66a3b-104">CEILING 関数</span><span class="sxs-lookup"><span data-stu-id="66a3b-104">CEILING Function</span></span>

<span data-ttu-id="66a3b-105">数値を 0 (ゼロ) から複数の次のインスタンスに切り上  _げします_。</span><span class="sxs-lookup"><span data-stu-id="66a3b-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="66a3b-106">multiple  _を_ 指定しない場合、数値は 0 から次の整数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="66a3b-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="66a3b-107">構文</span><span class="sxs-lookup"><span data-stu-id="66a3b-107">Syntax</span></span>

<span data-ttu-id="66a3b-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span><span class="sxs-lookup"><span data-stu-id="66a3b-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="66a3b-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="66a3b-109">Parameters</span></span>

|<span data-ttu-id="66a3b-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="66a3b-110">**Name**</span></span>|<span data-ttu-id="66a3b-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="66a3b-111">**Required/Optional**</span></span>|<span data-ttu-id="66a3b-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="66a3b-112">**Data Type**</span></span>|<span data-ttu-id="66a3b-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="66a3b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="66a3b-114">_number_</span><span class="sxs-lookup"><span data-stu-id="66a3b-114">_number_</span></span> <br/> |<span data-ttu-id="66a3b-115">必須</span><span class="sxs-lookup"><span data-stu-id="66a3b-115">Required</span></span>  <br/> |<span data-ttu-id="66a3b-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="66a3b-116">**Number**</span></span> <br/> |<span data-ttu-id="66a3b-117">切り上げの対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="66a3b-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="66a3b-118">_複数_</span><span class="sxs-lookup"><span data-stu-id="66a3b-118">_multiple_</span></span> <br/> |<span data-ttu-id="66a3b-119">必須</span><span class="sxs-lookup"><span data-stu-id="66a3b-119">Required</span></span>  <br/> |<span data-ttu-id="66a3b-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="66a3b-120">**Number**</span></span> <br/> |<span data-ttu-id="66a3b-121">倍数から切り上へ。</span><span class="sxs-lookup"><span data-stu-id="66a3b-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66a3b-122">注釈</span><span class="sxs-lookup"><span data-stu-id="66a3b-122">Remarks</span></span>

 <span data-ttu-id="66a3b-123">_数値_ と  _倍数は_ 、同じ記号、または複数の記号#NUM!</span><span class="sxs-lookup"><span data-stu-id="66a3b-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="66a3b-124">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="66a3b-124">error is returned.</span></span> <span data-ttu-id="66a3b-125">数値または  _複数_ の  _値_ に変換できない場合は、値#VALUE!</span><span class="sxs-lookup"><span data-stu-id="66a3b-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="66a3b-126">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="66a3b-126">error is returned.</span></span> <span data-ttu-id="66a3b-127">数値または _倍数__が_ 0 の場合、結果は 0 になります。</span><span class="sxs-lookup"><span data-stu-id="66a3b-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="66a3b-128">例 1</span><span class="sxs-lookup"><span data-stu-id="66a3b-128">Example 1</span></span>

<span data-ttu-id="66a3b-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="66a3b-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="66a3b-130">4 を返します</span><span class="sxs-lookup"><span data-stu-id="66a3b-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="66a3b-131">例 2</span><span class="sxs-lookup"><span data-stu-id="66a3b-131">Example 2</span></span>

<span data-ttu-id="66a3b-132">CEILING(-3.7)</span><span class="sxs-lookup"><span data-stu-id="66a3b-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="66a3b-133">-4 を返します</span><span class="sxs-lookup"><span data-stu-id="66a3b-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="66a3b-134">例 3</span><span class="sxs-lookup"><span data-stu-id="66a3b-134">Example 3</span></span>

<span data-ttu-id="66a3b-135">CEILING(3.7, 0.25)</span><span class="sxs-lookup"><span data-stu-id="66a3b-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="66a3b-136">3.75 を返します</span><span class="sxs-lookup"><span data-stu-id="66a3b-136">Returns 3.75</span></span>
  

