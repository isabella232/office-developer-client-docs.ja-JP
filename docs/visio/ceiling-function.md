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
description: 次の複数のインスタンスには、0 (ゼロ) から数値を丸めます。 複数を指定しない場合、次の整数を 0 から数に丸めます。
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804955"
---
# <a name="ceiling-function"></a><span data-ttu-id="fd616-104">CEILING 関数</span><span class="sxs-lookup"><span data-stu-id="fd616-104">CEILING Function</span></span>

<span data-ttu-id="fd616-105">_複数_の次のインスタンスを 0 (ゼロ) から数値を四捨五入します。</span><span class="sxs-lookup"><span data-stu-id="fd616-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="fd616-106">_複数_を指定しない場合、次の整数に 0 から番号を丸めます。</span><span class="sxs-lookup"><span data-stu-id="fd616-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fd616-107">構文</span><span class="sxs-lookup"><span data-stu-id="fd616-107">Syntax</span></span>

<span data-ttu-id="fd616-108">天井 (* **番号** *、* **複数** *)</span><span class="sxs-lookup"><span data-stu-id="fd616-108">CEILING(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fd616-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="fd616-109">Parameters</span></span>

|<span data-ttu-id="fd616-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="fd616-110">**Name**</span></span>|<span data-ttu-id="fd616-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="fd616-111">**Required/Optional**</span></span>|<span data-ttu-id="fd616-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="fd616-112">**Data Type**</span></span>|<span data-ttu-id="fd616-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="fd616-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fd616-114">_number_</span><span class="sxs-lookup"><span data-stu-id="fd616-114">_number_</span></span> <br/> |<span data-ttu-id="fd616-115">必須</span><span class="sxs-lookup"><span data-stu-id="fd616-115">Required</span></span>  <br/> |<span data-ttu-id="fd616-116">**番号**</span><span class="sxs-lookup"><span data-stu-id="fd616-116">**Number**</span></span> <br/> |<span data-ttu-id="fd616-117">切り上げの対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd616-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="fd616-118">_複数_</span><span class="sxs-lookup"><span data-stu-id="fd616-118">_multiple_</span></span> <br/> |<span data-ttu-id="fd616-119">必須</span><span class="sxs-lookup"><span data-stu-id="fd616-119">Required</span></span>  <br/> |<span data-ttu-id="fd616-120">**番号**</span><span class="sxs-lookup"><span data-stu-id="fd616-120">**Number**</span></span> <br/> |<span data-ttu-id="fd616-121">丸めを行う複数。</span><span class="sxs-lookup"><span data-stu-id="fd616-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd616-122">備考</span><span class="sxs-lookup"><span data-stu-id="fd616-122">Remarks</span></span>

 <span data-ttu-id="fd616-123">_番号_と_複数_は、同一の記号、または、#NUM を持つ必要があります!</span><span class="sxs-lookup"><span data-stu-id="fd616-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="fd616-124">エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="fd616-124">error is returned.</span></span> <span data-ttu-id="fd616-125">#Value! の値には、_番号_または_複数_のいずれかを変換できません! 場合、</span><span class="sxs-lookup"><span data-stu-id="fd616-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="fd616-126">エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="fd616-126">error is returned.</span></span> <span data-ttu-id="fd616-127">_番号_または_複数_のいずれかが 0 の場合、結果は 0 になります。</span><span class="sxs-lookup"><span data-stu-id="fd616-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fd616-128">例 1</span><span class="sxs-lookup"><span data-stu-id="fd616-128">Example 1</span></span>

<span data-ttu-id="fd616-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="fd616-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="fd616-130">4 を返します</span><span class="sxs-lookup"><span data-stu-id="fd616-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fd616-131">例 2</span><span class="sxs-lookup"><span data-stu-id="fd616-131">Example 2</span></span>

<span data-ttu-id="fd616-132">CEILING(-3.7)</span><span class="sxs-lookup"><span data-stu-id="fd616-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="fd616-133">-4 を返します</span><span class="sxs-lookup"><span data-stu-id="fd616-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fd616-134">例 3</span><span class="sxs-lookup"><span data-stu-id="fd616-134">Example 3</span></span>

<span data-ttu-id="fd616-135">天井 (3.7, 0.25)</span><span class="sxs-lookup"><span data-stu-id="fd616-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="fd616-136">3.75 を返します</span><span class="sxs-lookup"><span data-stu-id="fd616-136">Returns 3.75</span></span>
  

