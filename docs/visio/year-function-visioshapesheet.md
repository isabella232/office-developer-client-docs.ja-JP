---
title: YEAR 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: 日時または式を短い形式の日付でシステムの現在の地域と言語の設定の形式のグレゴリオ暦における年を表す整数を返します。
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806846"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="70f0c-103">YEAR 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="70f0c-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="70f0c-104">_日時_または_式_を短い形式の日付でシステムの現在の地域と言語の設定の形式のグレゴリオ暦における年を表す整数を返します。</span><span class="sxs-lookup"><span data-stu-id="70f0c-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="70f0c-105">構文</span><span class="sxs-lookup"><span data-stu-id="70f0c-105">Syntax</span></span>

<span data-ttu-id="70f0c-106">年 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="70f0c-106">YEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="70f0c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="70f0c-107">Parameters</span></span>

|<span data-ttu-id="70f0c-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="70f0c-108">**Name**</span></span>|<span data-ttu-id="70f0c-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="70f0c-109">**Required/Optional**</span></span>|<span data-ttu-id="70f0c-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="70f0c-110">**Data Type**</span></span>|<span data-ttu-id="70f0c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="70f0c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="70f0c-112">_日付時刻_</span><span class="sxs-lookup"><span data-stu-id="70f0c-112">_datetime_</span></span> <br/> |<span data-ttu-id="70f0c-113">必須</span><span class="sxs-lookup"><span data-stu-id="70f0c-113">Required</span></span>  <br/> |<span data-ttu-id="70f0c-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="70f0c-114">**String**</span></span> <br/> | <span data-ttu-id="70f0c-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="70f0c-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="70f0c-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="70f0c-116">_expression_</span></span> <br/> |<span data-ttu-id="70f0c-117">必須</span><span class="sxs-lookup"><span data-stu-id="70f0c-117">Required</span></span>  <br/> |<span data-ttu-id="70f0c-118">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="70f0c-118">**Varies**</span></span> <br/> |<span data-ttu-id="70f0c-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="70f0c-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="70f0c-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="70f0c-120">_lcid_</span></span> <br/> |<span data-ttu-id="70f0c-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="70f0c-121">Optional</span></span>  <br/> |<span data-ttu-id="70f0c-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="70f0c-122">**Numeric**</span></span> <br/> |<span data-ttu-id="70f0c-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="70f0c-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="70f0c-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="70f0c-125">Return value</span></span>

<span data-ttu-id="70f0c-126">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="70f0c-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70f0c-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="70f0c-127">Remarks</span></span>

<span data-ttu-id="70f0c-128">_日時_または_式_の時間の構成要素は破棄されます。</span><span class="sxs-lookup"><span data-stu-id="70f0c-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="70f0c-129">丸めは行われません。</span><span class="sxs-lookup"><span data-stu-id="70f0c-129">No rounding is done.</span></span> <span data-ttu-id="70f0c-130">_Datetime_が存在しないか、有効な日付または時刻として解釈できない場合、年には、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="70f0c-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="70f0c-131">YEAR 関数では、結果の整数部分が、1899 年 12 月 30 日以降の日数を表す_式_の 1 つの数値値も受け付けます。</span><span class="sxs-lookup"><span data-stu-id="70f0c-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="70f0c-132">例 1</span><span class="sxs-lookup"><span data-stu-id="70f0c-132">Example 1</span></span>

<span data-ttu-id="70f0c-133">YEAR("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="70f0c-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="70f0c-134">2007 を返します。</span><span class="sxs-lookup"><span data-stu-id="70f0c-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="70f0c-135">例 2</span><span class="sxs-lookup"><span data-stu-id="70f0c-135">Example 2</span></span>

<span data-ttu-id="70f0c-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="70f0c-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="70f0c-137">2007 を返します。</span><span class="sxs-lookup"><span data-stu-id="70f0c-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="70f0c-138">例 3</span><span class="sxs-lookup"><span data-stu-id="70f0c-138">Example 3</span></span>

<span data-ttu-id="70f0c-139">YEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="70f0c-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="70f0c-140">1997 を返します。</span><span class="sxs-lookup"><span data-stu-id="70f0c-140">Returns 1997.</span></span>
  

