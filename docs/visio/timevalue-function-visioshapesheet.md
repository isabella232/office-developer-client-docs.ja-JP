---
title: TIMEVALUE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: システムの地域と言語の設定に基づいて、datetime または expression で表される時刻値を返します。
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361111"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="fd197-103">TIMEVALUE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fd197-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fd197-104">システムの地域と言語の設定に基づいて、 _datetime_または_expression_で表される時刻値を返します。</span><span class="sxs-lookup"><span data-stu-id="fd197-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fd197-105">構文</span><span class="sxs-lookup"><span data-stu-id="fd197-105">Syntax</span></span>

<span data-ttu-id="fd197-106">timevalue ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="fd197-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fd197-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fd197-107">Parameters</span></span>

|<span data-ttu-id="fd197-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="fd197-108">**Name**</span></span>|<span data-ttu-id="fd197-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="fd197-109">**Required/Optional**</span></span>|<span data-ttu-id="fd197-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="fd197-110">**Data Type**</span></span>|<span data-ttu-id="fd197-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="fd197-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fd197-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="fd197-112">_datetime_</span></span> <br/> |<span data-ttu-id="fd197-113">必須</span><span class="sxs-lookup"><span data-stu-id="fd197-113">Required</span></span>  <br/> |<span data-ttu-id="fd197-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fd197-114">**String**</span></span> <br/> | <span data-ttu-id="fd197-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd197-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="fd197-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="fd197-116">_expression_</span></span> <br/> |<span data-ttu-id="fd197-117">必須</span><span class="sxs-lookup"><span data-stu-id="fd197-117">Required</span></span>  <br/> |<span data-ttu-id="fd197-118">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="fd197-118">**Varies**</span></span> <br/> | <span data-ttu-id="fd197-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd197-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="fd197-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="fd197-120">_lcid_</span></span> <br/> |<span data-ttu-id="fd197-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="fd197-121">Optional</span></span>  <br/> |<span data-ttu-id="fd197-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="fd197-122">**Number**</span></span> <br/> |<span data-ttu-id="fd197-123">現地以外の日時を計算するときに使用するロケール識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd197-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="fd197-124">ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="fd197-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd197-125">解説</span><span class="sxs-lookup"><span data-stu-id="fd197-125">Remarks</span></span>

<span data-ttu-id="fd197-126">_datetime_または_expression_の日付コンポーネントはすべて無視されます。</span><span class="sxs-lookup"><span data-stu-id="fd197-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="fd197-127">_datetime_が指定されていない場合、または有効な結果に変換できない場合は、この関数は #VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="fd197-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="fd197-128">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="fd197-128">error.</span></span> 
  
<span data-ttu-id="fd197-129">timevalue 関数では、 _expression_に単一の数値を使用することもできます。この場合、結果の10進部分には午前0時からの1日の小数部分を表します。</span><span class="sxs-lookup"><span data-stu-id="fd197-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fd197-130">例 1</span><span class="sxs-lookup"><span data-stu-id="fd197-130">Example 1</span></span>

<span data-ttu-id="fd197-131">TIMEVALUE("6:00 AM")</span><span class="sxs-lookup"><span data-stu-id="fd197-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="fd197-132">6:00 AM を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="fd197-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fd197-133">例 2</span><span class="sxs-lookup"><span data-stu-id="fd197-133">Example 2</span></span>

<span data-ttu-id="fd197-134">TIMEVALUE("14:30")+4 eh.+30 em.</span><span class="sxs-lookup"><span data-stu-id="fd197-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="fd197-135">19:00:00 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="fd197-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fd197-136">例 3</span><span class="sxs-lookup"><span data-stu-id="fd197-136">Example 3</span></span>

<span data-ttu-id="fd197-137">TIMEVALUE("11 AM, July 1, 1997")</span><span class="sxs-lookup"><span data-stu-id="fd197-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="fd197-138">11:00 AM を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="fd197-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="fd197-139">例 4</span><span class="sxs-lookup"><span data-stu-id="fd197-139">Example 4</span></span>

<span data-ttu-id="fd197-140">timevalue (0.6337)</span><span class="sxs-lookup"><span data-stu-id="fd197-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="fd197-141">15:12:32 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="fd197-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="fd197-142">例 5</span><span class="sxs-lookup"><span data-stu-id="fd197-142">Example 5</span></span>

<span data-ttu-id="fd197-143">timevalue ("7:89")</span><span class="sxs-lookup"><span data-stu-id="fd197-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="fd197-p103">#VALUE! エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="fd197-p103">Returns a #VALUE! error.</span></span>
  

