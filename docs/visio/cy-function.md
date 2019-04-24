---
title: CY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: 通貨値を返します。
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344990"
---
# <a name="cy-function"></a><span data-ttu-id="78eb5-103">CY 関数</span><span class="sxs-lookup"><span data-stu-id="78eb5-103">CY Function</span></span>

<span data-ttu-id="78eb5-104">通貨値を返します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="78eb5-105">構文</span><span class="sxs-lookup"><span data-stu-id="78eb5-105">Syntax</span></span>

<span data-ttu-id="78eb5-106">CY (\* **値** *、* \* *cyid* \* \*)</span><span class="sxs-lookup"><span data-stu-id="78eb5-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="78eb5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="78eb5-107">Parameters</span></span>

|<span data-ttu-id="78eb5-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="78eb5-108">**Name**</span></span>|<span data-ttu-id="78eb5-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="78eb5-109">**Required/Optional**</span></span>|<span data-ttu-id="78eb5-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="78eb5-110">**Data Type**</span></span>|<span data-ttu-id="78eb5-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="78eb5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="78eb5-112">_value_</span><span class="sxs-lookup"><span data-stu-id="78eb5-112">_value_</span></span> <br/> |<span data-ttu-id="78eb5-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="78eb5-113">Optional</span></span>  <br/> |<span data-ttu-id="78eb5-114">**Number または String**</span><span class="sxs-lookup"><span data-stu-id="78eb5-114">**Number or String**</span></span> <br/> |<span data-ttu-id="78eb5-115">通貨固有の書式設定を含む数値または文字列。</span><span class="sxs-lookup"><span data-stu-id="78eb5-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="78eb5-116">指定しない場合、通貨の値は、システムの地域と言語の設定の通貨スタイルに従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="78eb5-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="78eb5-117">_cyid_</span><span class="sxs-lookup"><span data-stu-id="78eb5-117">_cyID_</span></span> <br/> |<span data-ttu-id="78eb5-118">省略可能</span><span class="sxs-lookup"><span data-stu-id="78eb5-118">Optional</span></span>  <br/> |<span data-ttu-id="78eb5-119">**数値**</span><span class="sxs-lookup"><span data-stu-id="78eb5-119">**Number**</span></span> <br/> |<span data-ttu-id="78eb5-120">通貨 ID、または ISO 4217 の省略形を表す3文字の引用符で区切られた文字列。</span><span class="sxs-lookup"><span data-stu-id="78eb5-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78eb5-121">解説</span><span class="sxs-lookup"><span data-stu-id="78eb5-121">Remarks</span></span>

<span data-ttu-id="78eb5-122">別の通貨を指定するには、有効な_cyid_を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="78eb5-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="78eb5-123">通貨の一覧については、「[通貨定数について](about-currency-constants.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78eb5-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="78eb5-124">_value_が指定した通貨の種類と互換性がない場合、または "not not number" などの無効な引数が指定されている場合は、#VALUE します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="78eb5-125">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-125">error is returned.</span></span> <span data-ttu-id="78eb5-126">_値_が922337203685477.5807 より大きい場合、または-922337203685477.5808 未満の場合は、#VALUE します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="78eb5-127">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-127">error is returned.</span></span> 
  
<span data-ttu-id="78eb5-128">単位の分数 (3兆6000億など) を含む非常に大きな通貨の値を使用した場合の精度を向上させるには、 _value_に文字列引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="78eb5-129">無効な_cyid_を指定すると、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="78eb5-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="78eb5-130">例 1</span><span class="sxs-lookup"><span data-stu-id="78eb5-130">Example 1</span></span>

<span data-ttu-id="78eb5-131">ユーザーの [地域と言語] 設定で米国ドルが指定されている場合:</span><span class="sxs-lookup"><span data-stu-id="78eb5-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="78eb5-132">CY (999998.993)</span><span class="sxs-lookup"><span data-stu-id="78eb5-132">CY(999998.993)</span></span>
  
<span data-ttu-id="78eb5-133">$999,998.99 を返します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="78eb5-134">例 2</span><span class="sxs-lookup"><span data-stu-id="78eb5-134">Example 2</span></span>

<span data-ttu-id="78eb5-135">CY(12345678.993, "USD")</span><span class="sxs-lookup"><span data-stu-id="78eb5-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="78eb5-136">$12,345,678.99 を返します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="78eb5-137">例 3</span><span class="sxs-lookup"><span data-stu-id="78eb5-137">Example 3</span></span>

<span data-ttu-id="78eb5-138">CY(12345678.993, "DEM")</span><span class="sxs-lookup"><span data-stu-id="78eb5-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="78eb5-139">12,345,678.99 DEM を返します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="78eb5-140">例 4</span><span class="sxs-lookup"><span data-stu-id="78eb5-140">Example 4</span></span>

<span data-ttu-id="78eb5-141">CY(12345678.7832, "XXX")</span><span class="sxs-lookup"><span data-stu-id="78eb5-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="78eb5-142">12,345,678.78 を返します。</span><span class="sxs-lookup"><span data-stu-id="78eb5-142">Returns 12,345,678.78</span></span>
  

