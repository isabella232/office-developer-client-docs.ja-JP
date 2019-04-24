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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285245"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="16e80-103">WEEKDAY 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="16e80-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="16e80-104">_datetime_または_expression_の曜日を表す 1 ~ 7 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="16e80-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="16e80-105">構文</span><span class="sxs-lookup"><span data-stu-id="16e80-105">Syntax</span></span>

<span data-ttu-id="16e80-106">WEEKDAY ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="16e80-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="16e80-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="16e80-107">Parameters</span></span>

|<span data-ttu-id="16e80-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="16e80-108">**Name**</span></span>|<span data-ttu-id="16e80-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="16e80-109">**Required/Optional**</span></span>|<span data-ttu-id="16e80-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="16e80-110">**Data Type**</span></span>|<span data-ttu-id="16e80-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="16e80-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="16e80-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="16e80-112">_datetime_</span></span> <br/> |<span data-ttu-id="16e80-113">必須</span><span class="sxs-lookup"><span data-stu-id="16e80-113">Required</span></span>  <br/> |<span data-ttu-id="16e80-114">**String**</span><span class="sxs-lookup"><span data-stu-id="16e80-114">**String**</span></span> <br/> | <span data-ttu-id="16e80-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="16e80-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="16e80-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="16e80-116">_expression_</span></span> <br/> |<span data-ttu-id="16e80-117">必須</span><span class="sxs-lookup"><span data-stu-id="16e80-117">Required</span></span>  <br/> |<span data-ttu-id="16e80-118">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="16e80-118">**Varies**</span></span> <br/> |<span data-ttu-id="16e80-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="16e80-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="16e80-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="16e80-120">_lcid_</span></span> <br/> |<span data-ttu-id="16e80-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="16e80-121">Optional</span></span>  <br/> |<span data-ttu-id="16e80-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="16e80-122">**Numeric**</span></span> <br/> |<span data-ttu-id="16e80-123">現地以外の日時を計算するときに使用するロケール識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="16e80-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="16e80-124">ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="16e80-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="16e80-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="16e80-125">Return value</span></span>

<span data-ttu-id="16e80-126">整数</span><span class="sxs-lookup"><span data-stu-id="16e80-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16e80-127">解説</span><span class="sxs-lookup"><span data-stu-id="16e80-127">Remarks</span></span>

<span data-ttu-id="16e80-128">_datetime_または_expression_の時刻コンポーネントは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="16e80-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="16e80-129">結果は月曜日 (1) から日曜日 (7) に対応します。</span><span class="sxs-lookup"><span data-stu-id="16e80-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="16e80-130">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="16e80-130">No rounding is done.</span></span> <span data-ttu-id="16e80-131">_datetime_が指定されていない場合、または有効な日付または時刻として解釈できない場合は、関数は #VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="16e80-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="16e80-132">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="16e80-132">error.</span></span> 
  
<span data-ttu-id="16e80-133">WEEKDAY 関数では、 _expression_に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="16e80-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="16e80-134">例 1</span><span class="sxs-lookup"><span data-stu-id="16e80-134">Example 1</span></span>

<span data-ttu-id="16e80-135">WEEKDAY("May 30, 1999")</span><span class="sxs-lookup"><span data-stu-id="16e80-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="16e80-136">7 を返します。</span><span class="sxs-lookup"><span data-stu-id="16e80-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="16e80-137">例 2</span><span class="sxs-lookup"><span data-stu-id="16e80-137">Example 2</span></span>

<span data-ttu-id="16e80-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span><span class="sxs-lookup"><span data-stu-id="16e80-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="16e80-139">2 を返します。</span><span class="sxs-lookup"><span data-stu-id="16e80-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="16e80-140">例 3</span><span class="sxs-lookup"><span data-stu-id="16e80-140">Example 3</span></span>

<span data-ttu-id="16e80-141">曜日 (35880.6337)</span><span class="sxs-lookup"><span data-stu-id="16e80-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="16e80-142">4 を返します。</span><span class="sxs-lookup"><span data-stu-id="16e80-142">Returns 4.</span></span>
  

