---
title: SIGN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: 数値の符号を表す値を返します。
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806501"
---
# <a name="sign-function"></a><span data-ttu-id="d70b6-103">SIGN 関数</span><span class="sxs-lookup"><span data-stu-id="d70b6-103">SIGN Function</span></span>

<span data-ttu-id="d70b6-104">数値の符号を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="d70b6-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d70b6-105">構文</span><span class="sxs-lookup"><span data-stu-id="d70b6-105">Syntax</span></span>

<span data-ttu-id="d70b6-106">記号 (* **番号** *、* **ファジー* * *)</span><span class="sxs-lookup"><span data-stu-id="d70b6-106">SIGN(** *number* **, ** *fuzz* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d70b6-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d70b6-107">Parameters</span></span>

|<span data-ttu-id="d70b6-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d70b6-108">**Name**</span></span>|<span data-ttu-id="d70b6-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d70b6-109">**Required/Optional**</span></span>|<span data-ttu-id="d70b6-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d70b6-110">**Data Type**</span></span>|<span data-ttu-id="d70b6-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d70b6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d70b6-112">_number_</span><span class="sxs-lookup"><span data-stu-id="d70b6-112">_number_</span></span> <br/> |<span data-ttu-id="d70b6-113">必須</span><span class="sxs-lookup"><span data-stu-id="d70b6-113">Required</span></span>  <br/> |<span data-ttu-id="d70b6-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="d70b6-114">**Numeric**</span></span> <br/> | <span data-ttu-id="d70b6-115">符号を確認する数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d70b6-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="d70b6-116">_ファジー_</span><span class="sxs-lookup"><span data-stu-id="d70b6-116">_fuzz_</span></span> <br/> |<span data-ttu-id="d70b6-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="d70b6-117">Optional</span></span>  <br/> |<span data-ttu-id="d70b6-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="d70b6-118">**Numeric**</span></span> <br/> |<span data-ttu-id="d70b6-119">指定した数値と 0 との誤差を指定します。数値と 0 の差がこの誤差以内である場合に、数値は 0 として扱われます。</span><span class="sxs-lookup"><span data-stu-id="d70b6-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d70b6-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d70b6-120">Return value</span></span>

<span data-ttu-id="d70b6-121">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="d70b6-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d70b6-122">注釈</span><span class="sxs-lookup"><span data-stu-id="d70b6-122">Remarks</span></span>

<span data-ttu-id="d70b6-123">SIGN 関数は、_数値_が正の場合に 1 を返します、負の_数_は、0 または-1 が_数値_の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d70b6-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="d70b6-124">Specifyin_誤差_の値は、計算がほぼゼロの場合、浮動小数点の丸めエラーを避けるために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d70b6-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="d70b6-125">_ファジー_値を指定しない場合は、1e-9 (0.000000001) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d70b6-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="d70b6-126">または図面を拡大すると、厳密な比較をするときに異なる値を指定することがあります。</span><span class="sxs-lookup"><span data-stu-id="d70b6-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d70b6-127">例 1</span><span class="sxs-lookup"><span data-stu-id="d70b6-127">Example 1</span></span>

<span data-ttu-id="d70b6-128">SIGN(-5)</span><span class="sxs-lookup"><span data-stu-id="d70b6-128">SIGN(-5)</span></span>
  
<span data-ttu-id="d70b6-129">-1 を返します。</span><span class="sxs-lookup"><span data-stu-id="d70b6-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d70b6-130">例 2</span><span class="sxs-lookup"><span data-stu-id="d70b6-130">Example 2</span></span>

<span data-ttu-id="d70b6-131">SIGN(0)</span><span class="sxs-lookup"><span data-stu-id="d70b6-131">SIGN(0)</span></span>
  
<span data-ttu-id="d70b6-132">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="d70b6-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d70b6-133">例 3</span><span class="sxs-lookup"><span data-stu-id="d70b6-133">Example 3</span></span>

<span data-ttu-id="d70b6-134">SIGN(0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="d70b6-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="d70b6-135">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="d70b6-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="d70b6-136">例 4</span><span class="sxs-lookup"><span data-stu-id="d70b6-136">Example 4</span></span>

<span data-ttu-id="d70b6-137">SIGN(0.00000000001,0)</span><span class="sxs-lookup"><span data-stu-id="d70b6-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="d70b6-138">1 を返します。</span><span class="sxs-lookup"><span data-stu-id="d70b6-138">Returns 1.</span></span>
  

