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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348952"
---
# <a name="bound-function"></a><span data-ttu-id="7b71e-103">BOUND 関数</span><span class="sxs-lookup"><span data-stu-id="7b71e-103">BOUND Function</span></span>

<span data-ttu-id="7b71e-104">1 つの範囲または複数の範囲にセルの値を制約します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7b71e-105">構文</span><span class="sxs-lookup"><span data-stu-id="7b71e-105">Syntax</span></span>

<span data-ttu-id="7b71e-106">BOUND (\* **値** *、* \* *type* \* *、* \* *ignore* \* *、* \* *value1* \* *、* \* *value2* \* \* \* \* \* [, ignore (n)、value1 (n)、value2 (n),...] \* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7b71e-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7b71e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b71e-107">Parameters</span></span>

|<span data-ttu-id="7b71e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="7b71e-108">**Name**</span></span>|<span data-ttu-id="7b71e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="7b71e-109">**Required/Optional**</span></span>|<span data-ttu-id="7b71e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="7b71e-110">**Data Type**</span></span>|<span data-ttu-id="7b71e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="7b71e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7b71e-112">_value_</span><span class="sxs-lookup"><span data-stu-id="7b71e-112">_value_</span></span> <br/> |<span data-ttu-id="7b71e-113">必須</span><span class="sxs-lookup"><span data-stu-id="7b71e-113">Required</span></span>  <br/> |<span data-ttu-id="7b71e-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="7b71e-114">**Numeric**</span></span> <br/> |<span data-ttu-id="7b71e-115">制約される現在の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="7b71e-116">_type_</span><span class="sxs-lookup"><span data-stu-id="7b71e-116">_type_</span></span> <br/> |<span data-ttu-id="7b71e-117">必須</span><span class="sxs-lookup"><span data-stu-id="7b71e-117">Required</span></span>  <br/> |<span data-ttu-id="7b71e-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="7b71e-118">**Numeric**</span></span> <br/> |<span data-ttu-id="7b71e-119">制約が包括的 (0) であるか、排他的 (1) であるか、または無効 (2) であるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="7b71e-120">_フォント_</span><span class="sxs-lookup"><span data-stu-id="7b71e-120">_ignore_</span></span> <br/> |<span data-ttu-id="7b71e-121">必須</span><span class="sxs-lookup"><span data-stu-id="7b71e-121">Required</span></span>  <br/> |<span data-ttu-id="7b71e-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7b71e-122">**Boolean**</span></span> <br/> | <span data-ttu-id="7b71e-123">TRUE を指定すると、範囲は無視されます。FALSE を指定すると、セルの値が範囲に制限されます。</span><span class="sxs-lookup"><span data-stu-id="7b71e-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="7b71e-124">_value1_</span><span class="sxs-lookup"><span data-stu-id="7b71e-124">_value1_</span></span> <br/> |<span data-ttu-id="7b71e-125">必須</span><span class="sxs-lookup"><span data-stu-id="7b71e-125">Required</span></span>  <br/> |<span data-ttu-id="7b71e-126">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="7b71e-126">**Numeric**</span></span> <br/> |<span data-ttu-id="7b71e-127">範囲内の最初の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="7b71e-128">_value2_</span><span class="sxs-lookup"><span data-stu-id="7b71e-128">_value2_</span></span> <br/> |<span data-ttu-id="7b71e-129">必須</span><span class="sxs-lookup"><span data-stu-id="7b71e-129">Required</span></span>  <br/> |<span data-ttu-id="7b71e-130">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="7b71e-130">**Numeric**</span></span> <br/> |<span data-ttu-id="7b71e-131">範囲内の 2 番目の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b71e-132">解説</span><span class="sxs-lookup"><span data-stu-id="7b71e-132">Remarks</span></span>

<span data-ttu-id="7b71e-133">bound 関数を使用して、セルの値を上限と下限に制限します。たとえば、最小または最大の高さより上または下に拡大してはならないオブジェクトを制御します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="7b71e-134">範囲または範囲を基準として、制約を包含または排他的にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7b71e-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="7b71e-135">現在の値を制約しないようにするには、 _type_パラメーターを 2 (無効) に設定します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="7b71e-136">複数の範囲を定義するには、 _ignore_、 _value1_、および_value2_の各パラメーターを複数回指定します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="7b71e-137">特定の範囲によって制約を無効にするには、 _ignore_パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="7b71e-138">BOUND 関数を含む数式は、その値が変更されても上書きされません。代わりに、数式は保持され、新しい値は_value_パラメーターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="7b71e-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7b71e-139">例 1</span><span class="sxs-lookup"><span data-stu-id="7b71e-139">Example 1</span></span>

<span data-ttu-id="7b71e-140">この例では、BOUND 関数を使用して、コントロール ハンドルを図形の境界ボックス内に保持します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="7b71e-141">コントロール X1 = BOUND (幅\*0.5、0、FALSE、幅\*0、幅\*1)</span><span class="sxs-lookup"><span data-stu-id="7b71e-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="7b71e-142">コントロール. Y1 = BOUND (高さ\*0.5、0、FALSE、高さ\*0、高さ\*1)</span><span class="sxs-lookup"><span data-stu-id="7b71e-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7b71e-143">例 2</span><span class="sxs-lookup"><span data-stu-id="7b71e-143">Example 2</span></span>

<span data-ttu-id="7b71e-144">この例では、BOUND 関数を使用して、図形の幅を 2 インチ、4 インチ、または 6 インチ に制約します。</span><span class="sxs-lookup"><span data-stu-id="7b71e-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="7b71e-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span><span class="sxs-lookup"><span data-stu-id="7b71e-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

