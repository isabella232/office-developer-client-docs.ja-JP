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
description: 日時または式では、時間値を表すを返しますベースのシステムの地域と言語を設定します。
ms.openlocfilehash: e75607d19dc7062af717823c13f580cb44c9406b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806653"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="6804d-103">TIMEVALUE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6804d-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6804d-104">_日時_または_式_を時間の値を表すを返しますベースのシステムの地域と言語を設定します。</span><span class="sxs-lookup"><span data-stu-id="6804d-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6804d-105">構文</span><span class="sxs-lookup"><span data-stu-id="6804d-105">Syntax</span></span>

<span data-ttu-id="6804d-106">TIMEVALUE ("* * *datetime* * *」。* **式** * [、* * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="6804d-106">TIMEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6804d-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="6804d-107">Parameters</span></span>

|<span data-ttu-id="6804d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6804d-108">**Name**</span></span>|<span data-ttu-id="6804d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6804d-109">**Required/Optional**</span></span>|<span data-ttu-id="6804d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6804d-110">**Data Type**</span></span>|<span data-ttu-id="6804d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6804d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6804d-112">_日付時刻_</span><span class="sxs-lookup"><span data-stu-id="6804d-112">_datetime_</span></span> <br/> |<span data-ttu-id="6804d-113">必須</span><span class="sxs-lookup"><span data-stu-id="6804d-113">Required</span></span>  <br/> |<span data-ttu-id="6804d-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6804d-114">**String**</span></span> <br/> | <span data-ttu-id="6804d-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="6804d-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="6804d-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="6804d-116">_expression_</span></span> <br/> |<span data-ttu-id="6804d-117">必須</span><span class="sxs-lookup"><span data-stu-id="6804d-117">Required</span></span>  <br/> |<span data-ttu-id="6804d-118">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="6804d-118">**Varies**</span></span> <br/> | <span data-ttu-id="6804d-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="6804d-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="6804d-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="6804d-120">_lcid_</span></span> <br/> |<span data-ttu-id="6804d-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="6804d-121">Optional</span></span>  <br/> |<span data-ttu-id="6804d-122">**番号**</span><span class="sxs-lookup"><span data-stu-id="6804d-122">**Number**</span></span> <br/> |<span data-ttu-id="6804d-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="6804d-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6804d-125">注釈</span><span class="sxs-lookup"><span data-stu-id="6804d-125">Remarks</span></span>

<span data-ttu-id="6804d-126">_日時_または_式_で任意の日付コンポーネントが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="6804d-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="6804d-127">_Datetime_が存在しないか、有効な結果に変換することはできません、する場合、この関数は、#VALUE を返す!</span><span class="sxs-lookup"><span data-stu-id="6804d-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="6804d-128">エラーです。</span><span class="sxs-lookup"><span data-stu-id="6804d-128">error.</span></span> 
  
<span data-ttu-id="6804d-129">TIMEVALUE 関数では、結果の小数部分が 1 日午前 0 時からの分数を表す_式_の 1 つの数値値も受け付けます。</span><span class="sxs-lookup"><span data-stu-id="6804d-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6804d-130">例 1</span><span class="sxs-lookup"><span data-stu-id="6804d-130">Example 1</span></span>

<span data-ttu-id="6804d-131">TIMEVALUE("6:00 AM")</span><span class="sxs-lookup"><span data-stu-id="6804d-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="6804d-132">6:00 AM を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="6804d-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6804d-133">例 2</span><span class="sxs-lookup"><span data-stu-id="6804d-133">Example 2</span></span>

<span data-ttu-id="6804d-134">TIMEVALUE("14:30")+4 eh.+30 em.</span><span class="sxs-lookup"><span data-stu-id="6804d-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="6804d-135">19:00:00 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="6804d-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6804d-136">例 3</span><span class="sxs-lookup"><span data-stu-id="6804d-136">Example 3</span></span>

<span data-ttu-id="6804d-137">TIMEVALUE("11 AM, July 1, 1997")</span><span class="sxs-lookup"><span data-stu-id="6804d-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="6804d-138">11:00 AM を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="6804d-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="6804d-139">例 4</span><span class="sxs-lookup"><span data-stu-id="6804d-139">Example 4</span></span>

<span data-ttu-id="6804d-140">TIMEVALUE(0.6337)</span><span class="sxs-lookup"><span data-stu-id="6804d-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="6804d-141">15:12:32 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="6804d-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="6804d-142">例 5</span><span class="sxs-lookup"><span data-stu-id="6804d-142">Example 5</span></span>

<span data-ttu-id="6804d-143">TIMEVALUE("7:89")</span><span class="sxs-lookup"><span data-stu-id="6804d-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="6804d-p103">#VALUE! エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="6804d-p103">Returns a #VALUE! error.</span></span>
  

