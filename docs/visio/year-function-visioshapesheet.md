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
description: datetime または expression のグレゴリオ暦の年を表す整数を返します。これは、システムの現在の地域と言語の設定によって設定された短い日付形式に従って書式設定されます。
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351654"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="0883f-103">YEAR 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="0883f-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="0883f-104">_datetime_または_expression_のグレゴリオ暦の年を表す整数を返します。これは、システムの現在の地域と言語の設定によって設定された短い日付形式に従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="0883f-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0883f-105">構文</span><span class="sxs-lookup"><span data-stu-id="0883f-105">Syntax</span></span>

<span data-ttu-id="0883f-106">YEAR ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="0883f-106">YEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0883f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0883f-107">Parameters</span></span>

|<span data-ttu-id="0883f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="0883f-108">**Name**</span></span>|<span data-ttu-id="0883f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0883f-109">**Required/Optional**</span></span>|<span data-ttu-id="0883f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0883f-110">**Data Type**</span></span>|<span data-ttu-id="0883f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0883f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0883f-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="0883f-112">_datetime_</span></span> <br/> |<span data-ttu-id="0883f-113">必須</span><span class="sxs-lookup"><span data-stu-id="0883f-113">Required</span></span>  <br/> |<span data-ttu-id="0883f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="0883f-114">**String**</span></span> <br/> | <span data-ttu-id="0883f-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="0883f-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="0883f-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="0883f-116">_expression_</span></span> <br/> |<span data-ttu-id="0883f-117">必須</span><span class="sxs-lookup"><span data-stu-id="0883f-117">Required</span></span>  <br/> |<span data-ttu-id="0883f-118">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="0883f-118">**Varies**</span></span> <br/> |<span data-ttu-id="0883f-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="0883f-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="0883f-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="0883f-120">_lcid_</span></span> <br/> |<span data-ttu-id="0883f-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="0883f-121">Optional</span></span>  <br/> |<span data-ttu-id="0883f-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="0883f-122">**Numeric**</span></span> <br/> |<span data-ttu-id="0883f-123">現地以外の日時を計算するときに使用するロケール識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="0883f-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="0883f-124">ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="0883f-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0883f-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="0883f-125">Return value</span></span>

<span data-ttu-id="0883f-126">整数</span><span class="sxs-lookup"><span data-stu-id="0883f-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0883f-127">解説</span><span class="sxs-lookup"><span data-stu-id="0883f-127">Remarks</span></span>

<span data-ttu-id="0883f-128">_datetime_または_expression_の時刻コンポーネントは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="0883f-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="0883f-129">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="0883f-129">No rounding is done.</span></span> <span data-ttu-id="0883f-130">_datetime_が指定されていない場合、または有効な日付または時刻として解釈できない場合、YEAR はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="0883f-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="0883f-131">YEAR 関数では、 _expression_に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0883f-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0883f-132">例 1</span><span class="sxs-lookup"><span data-stu-id="0883f-132">Example 1</span></span>

<span data-ttu-id="0883f-133">YEAR ("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="0883f-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="0883f-134">2007 を返します。</span><span class="sxs-lookup"><span data-stu-id="0883f-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0883f-135">例 2</span><span class="sxs-lookup"><span data-stu-id="0883f-135">Example 2</span></span>

<span data-ttu-id="0883f-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="0883f-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="0883f-137">2007 を返します。</span><span class="sxs-lookup"><span data-stu-id="0883f-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0883f-138">例 3</span><span class="sxs-lookup"><span data-stu-id="0883f-138">Example 3</span></span>

<span data-ttu-id="0883f-139">年 (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="0883f-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="0883f-140">1997 を返します。</span><span class="sxs-lookup"><span data-stu-id="0883f-140">Returns 1997.</span></span>
  

