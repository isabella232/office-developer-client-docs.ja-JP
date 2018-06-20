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
description: 日時または式の曜日を表す 1 ~ 7 の整数を返します。
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806789"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="5fdd4-103">WEEKDAY 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="5fdd4-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="5fdd4-104">_日時_または_式_の曜日を表す 1 ~ 7 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5fdd4-105">構文</span><span class="sxs-lookup"><span data-stu-id="5fdd4-105">Syntax</span></span>

<span data-ttu-id="5fdd4-106">平日 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="5fdd4-106">WEEKDAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5fdd4-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="5fdd4-107">Parameters</span></span>

|<span data-ttu-id="5fdd4-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="5fdd4-108">**Name**</span></span>|<span data-ttu-id="5fdd4-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5fdd4-109">**Required/Optional**</span></span>|<span data-ttu-id="5fdd4-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5fdd4-110">**Data Type**</span></span>|<span data-ttu-id="5fdd4-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5fdd4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5fdd4-112">_日付時刻_</span><span class="sxs-lookup"><span data-stu-id="5fdd4-112">_datetime_</span></span> <br/> |<span data-ttu-id="5fdd4-113">必須</span><span class="sxs-lookup"><span data-stu-id="5fdd4-113">Required</span></span>  <br/> |<span data-ttu-id="5fdd4-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="5fdd4-114">**String**</span></span> <br/> | <span data-ttu-id="5fdd4-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="5fdd4-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="5fdd4-116">_expression_</span></span> <br/> |<span data-ttu-id="5fdd4-117">必須</span><span class="sxs-lookup"><span data-stu-id="5fdd4-117">Required</span></span>  <br/> |<span data-ttu-id="5fdd4-118">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="5fdd4-118">**Varies**</span></span> <br/> |<span data-ttu-id="5fdd4-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="5fdd4-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="5fdd4-120">_lcid_</span></span> <br/> |<span data-ttu-id="5fdd4-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="5fdd4-121">Optional</span></span>  <br/> |<span data-ttu-id="5fdd4-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="5fdd4-122">**Numeric**</span></span> <br/> |<span data-ttu-id="5fdd4-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5fdd4-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5fdd4-125">Return value</span></span>

<span data-ttu-id="5fdd4-126">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="5fdd4-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fdd4-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="5fdd4-127">Remarks</span></span>

<span data-ttu-id="5fdd4-128">_日時_または_式_の時間の構成要素は破棄されます。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="5fdd4-129">結果は、(1) を月曜日から日曜日 (7) に対応します。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="5fdd4-130">丸めは行われません。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-130">No rounding is done.</span></span> <span data-ttu-id="5fdd4-131">_Datetime_が存在しないか、有効な日付または時刻として解釈できない場合、関数は #value! を返します。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="5fdd4-132">エラーです。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-132">error.</span></span> 
  
<span data-ttu-id="5fdd4-133">WEEKDAY 関数では、結果の整数部分が、1899 年 12 月 30 日以降の日数を表す_式_の 1 つの数値値も受け付けます。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5fdd4-134">例 1</span><span class="sxs-lookup"><span data-stu-id="5fdd4-134">Example 1</span></span>

<span data-ttu-id="5fdd4-135">WEEKDAY("May 30, 1999")</span><span class="sxs-lookup"><span data-stu-id="5fdd4-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="5fdd4-136">7 を返します。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5fdd4-137">例 2</span><span class="sxs-lookup"><span data-stu-id="5fdd4-137">Example 2</span></span>

<span data-ttu-id="5fdd4-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span><span class="sxs-lookup"><span data-stu-id="5fdd4-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="5fdd4-139">2 を返します。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5fdd4-140">例 3</span><span class="sxs-lookup"><span data-stu-id="5fdd4-140">Example 3</span></span>

<span data-ttu-id="5fdd4-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="5fdd4-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="5fdd4-142">4 を返します。</span><span class="sxs-lookup"><span data-stu-id="5fdd4-142">Returns 4.</span></span>
  

