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
description: 数値を 0 (ゼロ)、次の整数、または倍数の次のインスタンスに丸します。
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439899"
---
# <a name="floor-function"></a><span data-ttu-id="3a252-103">FLOOR 関数</span><span class="sxs-lookup"><span data-stu-id="3a252-103">FLOOR Function</span></span>

<span data-ttu-id="3a252-104">数値を 0 (ゼロ)、次の整数、または複数の次のインスタンスに丸  _められます_。</span><span class="sxs-lookup"><span data-stu-id="3a252-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3a252-105">構文</span><span class="sxs-lookup"><span data-stu-id="3a252-105">Syntax</span></span>

<span data-ttu-id="3a252-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span><span class="sxs-lookup"><span data-stu-id="3a252-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3a252-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3a252-107">Parameters</span></span>

|<span data-ttu-id="3a252-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="3a252-108">**Name**</span></span>|<span data-ttu-id="3a252-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3a252-109">**Required/Optional**</span></span>|<span data-ttu-id="3a252-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3a252-110">**Data Type**</span></span>|<span data-ttu-id="3a252-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3a252-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3a252-112">_number_</span><span class="sxs-lookup"><span data-stu-id="3a252-112">_number_</span></span> <br/> |<span data-ttu-id="3a252-113">必須</span><span class="sxs-lookup"><span data-stu-id="3a252-113">Required</span></span>  <br/> |<span data-ttu-id="3a252-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="3a252-114">**Number**</span></span> <br/> |<span data-ttu-id="3a252-115">切り上げの対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3a252-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="3a252-116">_複数_</span><span class="sxs-lookup"><span data-stu-id="3a252-116">_multiple_</span></span> <br/> |<span data-ttu-id="3a252-117">必須</span><span class="sxs-lookup"><span data-stu-id="3a252-117">Required</span></span>  <br/> |<span data-ttu-id="3a252-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="3a252-118">**Number**</span></span> <br/> |<span data-ttu-id="3a252-119">切り上げの対象となる倍数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3a252-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3a252-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="3a252-120">Return value</span></span>

<span data-ttu-id="3a252-121">番号</span><span class="sxs-lookup"><span data-stu-id="3a252-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a252-122">注釈</span><span class="sxs-lookup"><span data-stu-id="3a252-122">Remarks</span></span>

<span data-ttu-id="3a252-123">multiple  _を_ 指定しない場合、数値は 0 から次の整数に向かって丸められます。</span><span class="sxs-lookup"><span data-stu-id="3a252-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="3a252-124">_数値_ と  _倍数は_ 、同じ記号、または複数の記号#NUM!</span><span class="sxs-lookup"><span data-stu-id="3a252-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="3a252-125">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="3a252-125">error is returned.</span></span> <span data-ttu-id="3a252-126">数値または  _複数_ の  _値_ に変換できない場合は、値#VALUE!</span><span class="sxs-lookup"><span data-stu-id="3a252-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="3a252-127">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="3a252-127">error is returned.</span></span> <span data-ttu-id="3a252-128">数値または _倍数__が_ 0 の場合、結果は 0 になります。</span><span class="sxs-lookup"><span data-stu-id="3a252-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="3a252-129">例 1</span><span class="sxs-lookup"><span data-stu-id="3a252-129">Example 1</span></span>

<span data-ttu-id="3a252-130">FLOOR(3.7)</span><span class="sxs-lookup"><span data-stu-id="3a252-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="3a252-131">3 を返します。</span><span class="sxs-lookup"><span data-stu-id="3a252-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3a252-132">例 2</span><span class="sxs-lookup"><span data-stu-id="3a252-132">Example 2</span></span>

<span data-ttu-id="3a252-133">FLOOR(-3.7)</span><span class="sxs-lookup"><span data-stu-id="3a252-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="3a252-134">-3 を返します。</span><span class="sxs-lookup"><span data-stu-id="3a252-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3a252-135">例 3</span><span class="sxs-lookup"><span data-stu-id="3a252-135">Example 3</span></span>

<span data-ttu-id="3a252-136">FLOOR(3.7, 0.5)</span><span class="sxs-lookup"><span data-stu-id="3a252-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="3a252-137">3.5 を返します。</span><span class="sxs-lookup"><span data-stu-id="3a252-137">Returns 3.5.</span></span>
  

