---
title: DAYOFYEAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: datetime または expression の年の何日目かを表す、1 ~ 366 の整数を返します。 DAYOFYEAR 関数では、グレゴリオ暦が使用されます。
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360294"
---
# <a name="dayofyear-function"></a><span data-ttu-id="b69ab-104">DAYOFYEAR 関数</span><span class="sxs-lookup"><span data-stu-id="b69ab-104">DAYOFYEAR Function</span></span>

<span data-ttu-id="b69ab-105">_datetime_または_expression_の年の何日目かを表す、1 ~ 366 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="b69ab-105">Returns an integer, 1 to 366, that represents the sequential day of the year in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="b69ab-106">DAYOFYEAR 関数では、グレゴリオ暦が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b69ab-106">The DAYOFYEAR function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b69ab-107">構文</span><span class="sxs-lookup"><span data-stu-id="b69ab-107">Syntax</span></span>

<span data-ttu-id="b69ab-108">DAYOFYEAR ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="b69ab-108">DAYOFYEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b69ab-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b69ab-109">Parameters</span></span>

|<span data-ttu-id="b69ab-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="b69ab-110">**Name**</span></span>|<span data-ttu-id="b69ab-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="b69ab-111">**Required/Optional**</span></span>|<span data-ttu-id="b69ab-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="b69ab-112">**Data Type**</span></span>|<span data-ttu-id="b69ab-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="b69ab-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b69ab-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="b69ab-114">_datetime_</span></span> <br/> |<span data-ttu-id="b69ab-115">必須</span><span class="sxs-lookup"><span data-stu-id="b69ab-115">Required</span></span>  <br/> |<span data-ttu-id="b69ab-116">**String**</span><span class="sxs-lookup"><span data-stu-id="b69ab-116">**String**</span></span> <br/> |<span data-ttu-id="b69ab-117">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="b69ab-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="b69ab-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="b69ab-118">_expression_</span></span> <br/> |<span data-ttu-id="b69ab-119">必須</span><span class="sxs-lookup"><span data-stu-id="b69ab-119">Required</span></span>  <br/> |<span data-ttu-id="b69ab-120">**String**</span><span class="sxs-lookup"><span data-stu-id="b69ab-120">**String**</span></span> <br/> |<span data-ttu-id="b69ab-121">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="b69ab-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="b69ab-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="b69ab-122">_lcid_</span></span> <br/> |<span data-ttu-id="b69ab-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="b69ab-123">Optional</span></span>  <br/> |<span data-ttu-id="b69ab-124">**数値**</span><span class="sxs-lookup"><span data-stu-id="b69ab-124">**Number**</span></span> <br/> |<span data-ttu-id="b69ab-p103">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="b69ab-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b69ab-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="b69ab-127">Return value</span></span>

<span data-ttu-id="b69ab-128">整数</span><span class="sxs-lookup"><span data-stu-id="b69ab-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b69ab-129">解説</span><span class="sxs-lookup"><span data-stu-id="b69ab-129">Remarks</span></span>

<span data-ttu-id="b69ab-130">_datetime_または_expression_の時刻コンポーネントは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="b69ab-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="b69ab-131">結果は 1 月 1 日～ 12 月 31 日に対応します。</span><span class="sxs-lookup"><span data-stu-id="b69ab-131">The result corresponds to January 1 to December 31.</span></span> <span data-ttu-id="b69ab-132">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="b69ab-132">No rounding is done.</span></span> <span data-ttu-id="b69ab-133">_datetime_が指定されていない場合、または有効な日付または時刻として解釈できない場合は、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="b69ab-133">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns an error.</span></span> 
  
<span data-ttu-id="b69ab-134">DAYOFYEAR 関数では、 _expression_に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b69ab-134">The DAYOFYEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b69ab-135">例 1</span><span class="sxs-lookup"><span data-stu-id="b69ab-135">Example 1</span></span>

<span data-ttu-id="b69ab-136">DAYOFYEAR("May 30, 1997 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="b69ab-136">DAYOFYEAR("May 30, 1997 13:45:24")</span></span>
  
<span data-ttu-id="b69ab-137">150 を返します。</span><span class="sxs-lookup"><span data-stu-id="b69ab-137">Returns 150.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b69ab-138">例 2</span><span class="sxs-lookup"><span data-stu-id="b69ab-138">Example 2</span></span>

<span data-ttu-id="b69ab-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="b69ab-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="b69ab-140">157 を返します。</span><span class="sxs-lookup"><span data-stu-id="b69ab-140">Returns 157.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b69ab-141">例 3</span><span class="sxs-lookup"><span data-stu-id="b69ab-141">Example 3</span></span>

<span data-ttu-id="b69ab-142">DAYOFYEAR (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="b69ab-142">DAYOFYEAR(35580.6337)</span></span>
  
<span data-ttu-id="b69ab-143">150 を返します。</span><span class="sxs-lookup"><span data-stu-id="b69ab-143">Returns 150.</span></span>
  

