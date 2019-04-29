---
title: WEEKDAY 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: datetime または expression の曜日を表す 1 ~ 7 の整数を返します。
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404807"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="36a37-103">WEEKDAY 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="36a37-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="36a37-104">_datetime_または_expression_の曜日を表す 1 ~ 7 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="36a37-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="36a37-105">構文</span><span class="sxs-lookup"><span data-stu-id="36a37-105">Syntax</span></span>

<span data-ttu-id="36a37-106">WEEKDAY ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="36a37-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="36a37-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="36a37-107">Parameters</span></span>

|<span data-ttu-id="36a37-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="36a37-108">**Name**</span></span>|<span data-ttu-id="36a37-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="36a37-109">**Required/Optional**</span></span>|<span data-ttu-id="36a37-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="36a37-110">**Data Type**</span></span>|<span data-ttu-id="36a37-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="36a37-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="36a37-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="36a37-112">_datetime_</span></span> <br/> |<span data-ttu-id="36a37-113">必須</span><span class="sxs-lookup"><span data-stu-id="36a37-113">Required</span></span>  <br/> |<span data-ttu-id="36a37-114">**String**</span><span class="sxs-lookup"><span data-stu-id="36a37-114">**String**</span></span> <br/> | <span data-ttu-id="36a37-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="36a37-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="36a37-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="36a37-116">_expression_</span></span> <br/> |<span data-ttu-id="36a37-117">必須</span><span class="sxs-lookup"><span data-stu-id="36a37-117">Required</span></span>  <br/> |<span data-ttu-id="36a37-118">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="36a37-118">**Varies**</span></span> <br/> |<span data-ttu-id="36a37-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="36a37-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="36a37-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="36a37-120">_lcid_</span></span> <br/> |<span data-ttu-id="36a37-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="36a37-121">Optional</span></span>  <br/> |<span data-ttu-id="36a37-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="36a37-122">**Numeric**</span></span> <br/> |<span data-ttu-id="36a37-123">現地以外の日時を計算するときに使用するロケール識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="36a37-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="36a37-124">ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="36a37-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="36a37-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="36a37-125">Return value</span></span>

<span data-ttu-id="36a37-126">整数</span><span class="sxs-lookup"><span data-stu-id="36a37-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36a37-127">注釈</span><span class="sxs-lookup"><span data-stu-id="36a37-127">Remarks</span></span>

<span data-ttu-id="36a37-128">_datetime_または_expression_の時刻コンポーネントは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="36a37-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="36a37-129">結果は月曜日 (1) から日曜日 (7) に対応します。</span><span class="sxs-lookup"><span data-stu-id="36a37-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="36a37-130">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="36a37-130">No rounding is done.</span></span> <span data-ttu-id="36a37-131">_datetime_が指定されていない場合、または有効な日付または時刻として解釈できない場合は、関数は #VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="36a37-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="36a37-132">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="36a37-132">error.</span></span> 
  
<span data-ttu-id="36a37-133">WEEKDAY 関数では、 _expression_に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="36a37-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="36a37-134">例 1</span><span class="sxs-lookup"><span data-stu-id="36a37-134">Example 1</span></span>

<span data-ttu-id="36a37-135">WEEKDAY("May 30, 1999")</span><span class="sxs-lookup"><span data-stu-id="36a37-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="36a37-136">7 を返します。</span><span class="sxs-lookup"><span data-stu-id="36a37-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="36a37-137">例 2</span><span class="sxs-lookup"><span data-stu-id="36a37-137">Example 2</span></span>

<span data-ttu-id="36a37-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span><span class="sxs-lookup"><span data-stu-id="36a37-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="36a37-139">2 を返します。</span><span class="sxs-lookup"><span data-stu-id="36a37-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="36a37-140">例 3</span><span class="sxs-lookup"><span data-stu-id="36a37-140">Example 3</span></span>

<span data-ttu-id="36a37-141">曜日 (35880.6337)</span><span class="sxs-lookup"><span data-stu-id="36a37-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="36a37-142">4 を返します。</span><span class="sxs-lookup"><span data-stu-id="36a37-142">Returns 4.</span></span>
  

