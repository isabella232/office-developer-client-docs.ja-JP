---
title: DATETIME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: datetime または expression で表される日付と時刻の値を返します。
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360320"
---
# <a name="datetime-function"></a><span data-ttu-id="0d1a0-103">DATETIME 関数</span><span class="sxs-lookup"><span data-stu-id="0d1a0-103">DATETIME Function</span></span>

<span data-ttu-id="0d1a0-104">_datetime_または_expression_で表される日付と時刻の値を返します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0d1a0-105">構文</span><span class="sxs-lookup"><span data-stu-id="0d1a0-105">Syntax</span></span>

<span data-ttu-id="0d1a0-106">datetime ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="0d1a0-106">DATETIME(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0d1a0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d1a0-107">Parameters</span></span>

|<span data-ttu-id="0d1a0-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-108">**Name**</span></span>|<span data-ttu-id="0d1a0-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-109">**Required/Optional**</span></span>|<span data-ttu-id="0d1a0-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-110">**Data Type**</span></span>|<span data-ttu-id="0d1a0-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0d1a0-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="0d1a0-112">_datetime_</span></span> <br/> |<span data-ttu-id="0d1a0-113">必須</span><span class="sxs-lookup"><span data-stu-id="0d1a0-113">Required</span></span>  <br/> |<span data-ttu-id="0d1a0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-114">**String**</span></span> <br/> |<span data-ttu-id="0d1a0-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="0d1a0-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="0d1a0-116">_expression_</span></span> <br/> |<span data-ttu-id="0d1a0-117">必須</span><span class="sxs-lookup"><span data-stu-id="0d1a0-117">Required</span></span>  <br/> |<span data-ttu-id="0d1a0-118">**String**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-118">**String**</span></span> <br/> |<span data-ttu-id="0d1a0-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="0d1a0-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="0d1a0-120">_lcid_</span></span> <br/> |<span data-ttu-id="0d1a0-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d1a0-121">Optional</span></span>  <br/> |<span data-ttu-id="0d1a0-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-122">**Number**</span></span> <br/> |<span data-ttu-id="0d1a0-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0d1a0-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d1a0-125">Return value</span></span>

<span data-ttu-id="0d1a0-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="0d1a0-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d1a0-127">解説</span><span class="sxs-lookup"><span data-stu-id="0d1a0-127">Remarks</span></span>

<span data-ttu-id="0d1a0-128">*datetime*が指定されていない場合、または有効な日付または時刻として解釈できない場合は、datetime は #VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="0d1a0-129">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-129">error.</span></span> 
  
<span data-ttu-id="0d1a0-130">戻り値は、システムの現在の [地域] で設定されている短い日付と時刻の形式に従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="0d1a0-131">DATETIME 関数では、 *expression*に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定し、小数部分には午前0時からの日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0d1a0-132">例 1</span><span class="sxs-lookup"><span data-stu-id="0d1a0-132">Example 1</span></span>

<span data-ttu-id="0d1a0-133">DATETIME("May 30, 1997")+5 ed.</span><span class="sxs-lookup"><span data-stu-id="0d1a0-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="0d1a0-134">1997/6/4 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0d1a0-135">例 2</span><span class="sxs-lookup"><span data-stu-id="0d1a0-135">Example 2</span></span>

<span data-ttu-id="0d1a0-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span><span class="sxs-lookup"><span data-stu-id="0d1a0-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="0d1a0-137">文字列 "Tuesday, May 20, 1997 2:30:45 PM" を返します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0d1a0-138">例 3</span><span class="sxs-lookup"><span data-stu-id="0d1a0-138">Example 3</span></span>

<span data-ttu-id="0d1a0-139">DATETIME("1:30 PM July 19")</span><span class="sxs-lookup"><span data-stu-id="0d1a0-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="0d1a0-140">2001/7/19 午後 1:30:00 を表す値 (現在の年を 2001 とする) を返します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="0d1a0-141">例 4</span><span class="sxs-lookup"><span data-stu-id="0d1a0-141">Example 4</span></span>

<span data-ttu-id="0d1a0-142">DATETIME (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="0d1a0-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="0d1a0-143">1997/5/30 午後 3:12:32 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

