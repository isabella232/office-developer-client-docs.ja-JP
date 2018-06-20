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
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805136"
---
# <a name="cy-function"></a><span data-ttu-id="f249d-103">CY 関数</span><span class="sxs-lookup"><span data-stu-id="f249d-103">CY Function</span></span>

<span data-ttu-id="f249d-104">通貨値を返します。</span><span class="sxs-lookup"><span data-stu-id="f249d-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f249d-105">構文</span><span class="sxs-lookup"><span data-stu-id="f249d-105">Syntax</span></span>

<span data-ttu-id="f249d-106">CY (* **値** *、* * *cyID* * *)</span><span class="sxs-lookup"><span data-stu-id="f249d-106">CY(** *value* **, ** *cyID* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f249d-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f249d-107">Parameters</span></span>

|<span data-ttu-id="f249d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="f249d-108">**Name**</span></span>|<span data-ttu-id="f249d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f249d-109">**Required/Optional**</span></span>|<span data-ttu-id="f249d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f249d-110">**Data Type**</span></span>|<span data-ttu-id="f249d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="f249d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f249d-112">_value_</span><span class="sxs-lookup"><span data-stu-id="f249d-112">_value_</span></span> <br/> |<span data-ttu-id="f249d-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="f249d-113">Optional</span></span>  <br/> |<span data-ttu-id="f249d-114">**数値または文字列**</span><span class="sxs-lookup"><span data-stu-id="f249d-114">**Number or String**</span></span> <br/> |<span data-ttu-id="f249d-115">数値または通貨固有の書式設定を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="f249d-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="f249d-116">指定しない場合、通貨型の値はシステムの地域と言語の設定の通貨スタイルに従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="f249d-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="f249d-117">_cyid を指定_</span><span class="sxs-lookup"><span data-stu-id="f249d-117">_cyID_</span></span> <br/> |<span data-ttu-id="f249d-118">省略可能</span><span class="sxs-lookup"><span data-stu-id="f249d-118">Optional</span></span>  <br/> |<span data-ttu-id="f249d-119">**番号**</span><span class="sxs-lookup"><span data-stu-id="f249d-119">**Number**</span></span> <br/> |<span data-ttu-id="f249d-120">数値通貨 ID、または ISO 4217 の省略形の 3 文字の引用符で囲まれた文字列です。</span><span class="sxs-lookup"><span data-stu-id="f249d-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f249d-121">備考</span><span class="sxs-lookup"><span data-stu-id="f249d-121">Remarks</span></span>

<span data-ttu-id="f249d-122">別の通貨を指定するには、有効な_cyid を指定_する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f249d-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="f249d-123">一覧については、[通貨定数について](about-currency-constants.md)参照してください。</span><span class="sxs-lookup"><span data-stu-id="f249d-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="f249d-124">_値_は、通貨の種類と互換性がない場合、または「非数」などの無効な引数が指定されて、#value!!</span><span class="sxs-lookup"><span data-stu-id="f249d-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="f249d-125">エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="f249d-125">error is returned.</span></span> <span data-ttu-id="f249d-126">_値_が 922,337,203,685,477.5807 またはより少ない-922,337,203,685,477.5808、#value! より大きい場合は!</span><span class="sxs-lookup"><span data-stu-id="f249d-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="f249d-127">エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="f249d-127">error is returned.</span></span> 
  
<span data-ttu-id="f249d-128">精度 3.6 兆など、単位の小数点を含む非常に大きな通貨の値を向上させるには、_値_の文字列引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="f249d-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="f249d-129">無効な_cyID_を指定するには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="f249d-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f249d-130">例 1</span><span class="sxs-lookup"><span data-stu-id="f249d-130">Example 1</span></span>

<span data-ttu-id="f249d-131">ユーザーの [地域と言語] 設定で米国ドルが指定されている場合:</span><span class="sxs-lookup"><span data-stu-id="f249d-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="f249d-132">CY(999998.993)</span><span class="sxs-lookup"><span data-stu-id="f249d-132">CY(999998.993)</span></span>
  
<span data-ttu-id="f249d-133">$999,998.99 を返します。</span><span class="sxs-lookup"><span data-stu-id="f249d-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f249d-134">例 2</span><span class="sxs-lookup"><span data-stu-id="f249d-134">Example 2</span></span>

<span data-ttu-id="f249d-135">CY(12345678.993, "USD")</span><span class="sxs-lookup"><span data-stu-id="f249d-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="f249d-136">$12,345,678.99 を返します。</span><span class="sxs-lookup"><span data-stu-id="f249d-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f249d-137">例 3</span><span class="sxs-lookup"><span data-stu-id="f249d-137">Example 3</span></span>

<span data-ttu-id="f249d-138">CY(12345678.993, "DEM")</span><span class="sxs-lookup"><span data-stu-id="f249d-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="f249d-139">12,345,678.99 DEM を返します。</span><span class="sxs-lookup"><span data-stu-id="f249d-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="f249d-140">例 4</span><span class="sxs-lookup"><span data-stu-id="f249d-140">Example 4</span></span>

<span data-ttu-id="f249d-141">CY(12345678.7832, "XXX")</span><span class="sxs-lookup"><span data-stu-id="f249d-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="f249d-142">12,345,678.78 を返します。</span><span class="sxs-lookup"><span data-stu-id="f249d-142">Returns 12,345,678.78</span></span>
  

