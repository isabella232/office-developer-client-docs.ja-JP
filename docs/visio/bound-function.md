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
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804949"
---
# <a name="bound-function"></a><span data-ttu-id="e1e42-103">BOUND 関数</span><span class="sxs-lookup"><span data-stu-id="e1e42-103">BOUND Function</span></span>

<span data-ttu-id="e1e42-104">1 つの範囲または複数の範囲にセルの値を制約します。</span><span class="sxs-lookup"><span data-stu-id="e1e42-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e1e42-105">構文</span><span class="sxs-lookup"><span data-stu-id="e1e42-105">Syntax</span></span>

<span data-ttu-id="e1e42-106">バインド (* **値** *、* **型** *、* **無視** *、* * *value1* * *、* **値 2* * * * * * [、ignore(n)、value1(n)、value2(n)、...] * * *)</span><span class="sxs-lookup"><span data-stu-id="e1e42-106">BOUND (** *value* **, ** *type* **, ** *ignore* **, ** *value1* **, ** *value2* ** ** * [,ignore(n), value1(n), value2(n),...] * ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e1e42-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e1e42-107">Parameters</span></span>

|<span data-ttu-id="e1e42-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="e1e42-108">**Name**</span></span>|<span data-ttu-id="e1e42-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e1e42-109">**Required/Optional**</span></span>|<span data-ttu-id="e1e42-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e1e42-110">**Data Type**</span></span>|<span data-ttu-id="e1e42-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="e1e42-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e1e42-112">_value_</span><span class="sxs-lookup"><span data-stu-id="e1e42-112">_value_</span></span> <br/> |<span data-ttu-id="e1e42-113">必須</span><span class="sxs-lookup"><span data-stu-id="e1e42-113">Required</span></span>  <br/> |<span data-ttu-id="e1e42-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="e1e42-114">**Numeric**</span></span> <br/> |<span data-ttu-id="e1e42-115">制約される現在の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e1e42-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="e1e42-116">_type_</span><span class="sxs-lookup"><span data-stu-id="e1e42-116">_type_</span></span> <br/> |<span data-ttu-id="e1e42-117">必須</span><span class="sxs-lookup"><span data-stu-id="e1e42-117">Required</span></span>  <br/> |<span data-ttu-id="e1e42-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="e1e42-118">**Numeric**</span></span> <br/> |<span data-ttu-id="e1e42-119">制約が包括的 (0) であるか、排他的 (1) であるか、または無効 (2) であるかを指定します。
</span><span class="sxs-lookup"><span data-stu-id="e1e42-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="e1e42-120">_無視します。_</span><span class="sxs-lookup"><span data-stu-id="e1e42-120">_ignore_</span></span> <br/> |<span data-ttu-id="e1e42-121">必須</span><span class="sxs-lookup"><span data-stu-id="e1e42-121">Required</span></span>  <br/> |<span data-ttu-id="e1e42-122">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="e1e42-122">**Boolean**</span></span> <br/> | <span data-ttu-id="e1e42-123">範囲を無視する場合は TRUE。範囲にセルの値を制約する場合は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="e1e42-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="e1e42-124">_値 1_</span><span class="sxs-lookup"><span data-stu-id="e1e42-124">_value1_</span></span> <br/> |<span data-ttu-id="e1e42-125">必須</span><span class="sxs-lookup"><span data-stu-id="e1e42-125">Required</span></span>  <br/> |<span data-ttu-id="e1e42-126">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="e1e42-126">**Numeric**</span></span> <br/> |<span data-ttu-id="e1e42-127">範囲内の最初の値を指定します。
</span><span class="sxs-lookup"><span data-stu-id="e1e42-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="e1e42-128">_値 2_</span><span class="sxs-lookup"><span data-stu-id="e1e42-128">_value2_</span></span> <br/> |<span data-ttu-id="e1e42-129">必須</span><span class="sxs-lookup"><span data-stu-id="e1e42-129">Required</span></span>  <br/> |<span data-ttu-id="e1e42-130">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="e1e42-130">**Numeric**</span></span> <br/> |<span data-ttu-id="e1e42-131">範囲内の 2 番目の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e1e42-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1e42-132">注釈</span><span class="sxs-lookup"><span data-stu-id="e1e42-132">Remarks</span></span>

<span data-ttu-id="e1e42-133">BOUND 関数を使用すると、セルの値を上限と下限値、たとえば、最小または最大の高さより上または下にない拡大するかのオブジェクトを制御するために制限できます。</span><span class="sxs-lookup"><span data-stu-id="e1e42-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="e1e42-134">制約は、包括的または排他的な範囲にあります。</span><span class="sxs-lookup"><span data-stu-id="e1e42-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="e1e42-135">現在の値を制限しない必要がある場合、2 の (無効) に_型_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="e1e42-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="e1e42-136">_無視_、 _value1_と_value2_のパラメーターの複数のオカレンスを指定することによって、複数の範囲を定義できます。</span><span class="sxs-lookup"><span data-stu-id="e1e42-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="e1e42-137">_無視する_パラメーターを使用して、特定の範囲による制約を無効にします。</span><span class="sxs-lookup"><span data-stu-id="e1e42-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="e1e42-138">BOUND 関数を含む数式がその値が変更されると上書きされません。代わりに、数式は保持し、新しい値が_value_パラメーターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="e1e42-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e1e42-139">例 1</span><span class="sxs-lookup"><span data-stu-id="e1e42-139">Example 1</span></span>

<span data-ttu-id="e1e42-140">この例では、BOUND 関数を使用して、コントロール ハンドルを図形の境界ボックス内に保持します。</span><span class="sxs-lookup"><span data-stu-id="e1e42-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="e1e42-141">Controls.X1 = バインド (幅\*0.5、0、FALSE、幅\*0、幅\*1)</span><span class="sxs-lookup"><span data-stu-id="e1e42-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="e1e42-142">Controls.Y1 = バインド (高さ\*0.5、0、FALSE、高さ\*0、高さ\*1)</span><span class="sxs-lookup"><span data-stu-id="e1e42-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e1e42-143">例 2</span><span class="sxs-lookup"><span data-stu-id="e1e42-143">Example 2</span></span>

<span data-ttu-id="e1e42-144">この例では、BOUND 関数を使用して、図形の幅を 2 インチ、4 インチ、または 6 インチ に制約します。</span><span class="sxs-lookup"><span data-stu-id="e1e42-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="e1e42-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span><span class="sxs-lookup"><span data-stu-id="e1e42-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

