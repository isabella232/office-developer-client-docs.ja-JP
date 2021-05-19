---
title: BOUND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: 1 つの範囲または複数の範囲にセルの値を制約します。
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425961"
---
# <a name="bound-function"></a><span data-ttu-id="1228a-103">BOUND 関数</span><span class="sxs-lookup"><span data-stu-id="1228a-103">BOUND Function</span></span>

<span data-ttu-id="1228a-104">1 つの範囲または複数の範囲にセルの値を制約します。</span><span class="sxs-lookup"><span data-stu-id="1228a-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1228a-105">構文</span><span class="sxs-lookup"><span data-stu-id="1228a-105">Syntax</span></span>

<span data-ttu-id="1228a-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* ignore \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* ) </span><span class="sxs-lookup"><span data-stu-id="1228a-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1228a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1228a-107">Parameters</span></span>

|<span data-ttu-id="1228a-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="1228a-108">**Name**</span></span>|<span data-ttu-id="1228a-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="1228a-109">**Required/Optional**</span></span>|<span data-ttu-id="1228a-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="1228a-110">**Data Type**</span></span>|<span data-ttu-id="1228a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="1228a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1228a-112">_value_</span><span class="sxs-lookup"><span data-stu-id="1228a-112">_value_</span></span> <br/> |<span data-ttu-id="1228a-113">必須</span><span class="sxs-lookup"><span data-stu-id="1228a-113">Required</span></span>  <br/> |<span data-ttu-id="1228a-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="1228a-114">**Numeric**</span></span> <br/> |<span data-ttu-id="1228a-115">制約される現在の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1228a-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="1228a-116">_type_</span><span class="sxs-lookup"><span data-stu-id="1228a-116">_type_</span></span> <br/> |<span data-ttu-id="1228a-117">必須</span><span class="sxs-lookup"><span data-stu-id="1228a-117">Required</span></span>  <br/> |<span data-ttu-id="1228a-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="1228a-118">**Numeric**</span></span> <br/> |<span data-ttu-id="1228a-119">制約が包括的 (0) であるか、排他的 (1) であるか、または無効 (2) であるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="1228a-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="1228a-120">_ignore_</span><span class="sxs-lookup"><span data-stu-id="1228a-120">_ignore_</span></span> <br/> |<span data-ttu-id="1228a-121">必須</span><span class="sxs-lookup"><span data-stu-id="1228a-121">Required</span></span>  <br/> |<span data-ttu-id="1228a-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1228a-122">**Boolean**</span></span> <br/> | <span data-ttu-id="1228a-123">範囲を無視する場合は TRUE。セルの値を範囲に制限するには、FALSE を指定します。</span><span class="sxs-lookup"><span data-stu-id="1228a-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="1228a-124">_value1_</span><span class="sxs-lookup"><span data-stu-id="1228a-124">_value1_</span></span> <br/> |<span data-ttu-id="1228a-125">必須</span><span class="sxs-lookup"><span data-stu-id="1228a-125">Required</span></span>  <br/> |<span data-ttu-id="1228a-126">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="1228a-126">**Numeric**</span></span> <br/> |<span data-ttu-id="1228a-127">範囲内の最初の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1228a-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="1228a-128">_value2_</span><span class="sxs-lookup"><span data-stu-id="1228a-128">_value2_</span></span> <br/> |<span data-ttu-id="1228a-129">必須</span><span class="sxs-lookup"><span data-stu-id="1228a-129">Required</span></span>  <br/> |<span data-ttu-id="1228a-130">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="1228a-130">**Numeric**</span></span> <br/> |<span data-ttu-id="1228a-131">範囲内の 2 番目の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1228a-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1228a-132">注釈</span><span class="sxs-lookup"><span data-stu-id="1228a-132">Remarks</span></span>

<span data-ttu-id="1228a-133">たとえば、セルの値を上限と下限に制限するには、BOUND 関数を使用して、最小または最大の高さの上下に伸ばさないオブジェクトを制御します。</span><span class="sxs-lookup"><span data-stu-id="1228a-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="1228a-134">この制約は、範囲または範囲に関して包括的または排他的に指定できます。</span><span class="sxs-lookup"><span data-stu-id="1228a-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="1228a-135">現在の値を制限しない場合は  _、type_ パラメーターを 2 (無効) に設定します。</span><span class="sxs-lookup"><span data-stu-id="1228a-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="1228a-136">複数の範囲を定義するには、ignore パラメーター _、value1 パラメーター、value2_ パラメーターを複数 _指定_ します。 </span><span class="sxs-lookup"><span data-stu-id="1228a-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="1228a-137">ignore パラメーター  _を使用_ して、特定の範囲の制約を無効にします。</span><span class="sxs-lookup"><span data-stu-id="1228a-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="1228a-138">BOUND 関数を含む数式は、値が変更しても上書きされません。代わりに、数式が保持され、新しい値が value パラメーターに  _配置_ されます。</span><span class="sxs-lookup"><span data-stu-id="1228a-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="1228a-139">例 1</span><span class="sxs-lookup"><span data-stu-id="1228a-139">Example 1</span></span>

<span data-ttu-id="1228a-140">この例では、BOUND 関数を使用して、コントロール ハンドルを図形の境界ボックス内に保持します。</span><span class="sxs-lookup"><span data-stu-id="1228a-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="1228a-141">Controls.X1 = BOUND(Width \* 0.5, 0, FALSE, Width \* 0, Width \* 1)</span><span class="sxs-lookup"><span data-stu-id="1228a-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="1228a-142">Controls.Y1 = BOUND(Height \* 0.5, 0, FALSE, Height \* 0, Height \* 1)</span><span class="sxs-lookup"><span data-stu-id="1228a-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1228a-143">例 2</span><span class="sxs-lookup"><span data-stu-id="1228a-143">Example 2</span></span>

<span data-ttu-id="1228a-144">この例では、BOUND 関数を使用して、図形の幅を 2 インチ、4 インチ、または 6 インチ に制約します。</span><span class="sxs-lookup"><span data-stu-id="1228a-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="1228a-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span><span class="sxs-lookup"><span data-stu-id="1228a-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

