---
title: DAY 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: 日時または式の曜日を表す 1 ~ 31 の整数を返します。 DAY 関数はグレゴリオ暦を使用します。
ms.openlocfilehash: 07607b809aec9f50ae8981476313fc5e8dbc3423
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805198"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="f33f7-104">DAY 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="f33f7-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="f33f7-105">_日時_または_式_の日を表す 1 ~ 31 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="f33f7-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="f33f7-106">DAY 関数はグレゴリオ暦を使用します。</span><span class="sxs-lookup"><span data-stu-id="f33f7-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f33f7-107">構文</span><span class="sxs-lookup"><span data-stu-id="f33f7-107">Syntax</span></span>

<span data-ttu-id="f33f7-108">日 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="f33f7-108">DAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f33f7-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f33f7-109">Parameters</span></span>

|<span data-ttu-id="f33f7-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="f33f7-110">**Name**</span></span>|<span data-ttu-id="f33f7-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f33f7-111">**Required/Optional**</span></span>|<span data-ttu-id="f33f7-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f33f7-112">**Data Type**</span></span>|<span data-ttu-id="f33f7-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="f33f7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f33f7-114">_日付時刻_</span><span class="sxs-lookup"><span data-stu-id="f33f7-114">_datetime_</span></span> <br/> |<span data-ttu-id="f33f7-115">必須</span><span class="sxs-lookup"><span data-stu-id="f33f7-115">Required</span></span>  <br/> |<span data-ttu-id="f33f7-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="f33f7-116">**String**</span></span> <br/> |<span data-ttu-id="f33f7-117">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="f33f7-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="f33f7-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="f33f7-118">_expression_</span></span> <br/> |<span data-ttu-id="f33f7-119">必須</span><span class="sxs-lookup"><span data-stu-id="f33f7-119">Required</span></span>  <br/> |<span data-ttu-id="f33f7-120">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="f33f7-120">**String**</span></span> <br/> |<span data-ttu-id="f33f7-121">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="f33f7-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="f33f7-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="f33f7-122">_lcid_</span></span> <br/> |<span data-ttu-id="f33f7-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="f33f7-123">Optional</span></span>  <br/> |<span data-ttu-id="f33f7-124">**番号**</span><span class="sxs-lookup"><span data-stu-id="f33f7-124">**Number**</span></span> <br/> |<span data-ttu-id="f33f7-p103">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="f33f7-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f33f7-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="f33f7-127">Return value</span></span>

<span data-ttu-id="f33f7-128">整数</span><span class="sxs-lookup"><span data-stu-id="f33f7-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f33f7-129">注釈</span><span class="sxs-lookup"><span data-stu-id="f33f7-129">Remarks</span></span>

<span data-ttu-id="f33f7-130">_日時_または_式_で任意の時間コンポーネントを破棄します。</span><span class="sxs-lookup"><span data-stu-id="f33f7-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="f33f7-131">丸めは行われません。</span><span class="sxs-lookup"><span data-stu-id="f33f7-131">No rounding is done.</span></span> <span data-ttu-id="f33f7-132">_Datetime_が存在しないか、有効な結果に変換することはできません、する場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="f33f7-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="f33f7-133">DAY 関数では、結果の整数部分が、1899 年 12 月 30 日以降の日数を表す_式_の 1 つの数値値も受け付けます。</span><span class="sxs-lookup"><span data-stu-id="f33f7-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f33f7-134">例 1</span><span class="sxs-lookup"><span data-stu-id="f33f7-134">Example 1</span></span>

<span data-ttu-id="f33f7-135">DAY("May 30, 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="f33f7-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="f33f7-136">30 を返します。</span><span class="sxs-lookup"><span data-stu-id="f33f7-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f33f7-137">例 2</span><span class="sxs-lookup"><span data-stu-id="f33f7-137">Example 2</span></span>

<span data-ttu-id="f33f7-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="f33f7-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="f33f7-139">6 を返します。</span><span class="sxs-lookup"><span data-stu-id="f33f7-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f33f7-140">例 3</span><span class="sxs-lookup"><span data-stu-id="f33f7-140">Example 3</span></span>

<span data-ttu-id="f33f7-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="f33f7-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="f33f7-142">30 を返します。</span><span class="sxs-lookup"><span data-stu-id="f33f7-142">Returns 30.</span></span>
  

