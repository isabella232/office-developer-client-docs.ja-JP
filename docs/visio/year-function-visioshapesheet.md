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
description: システムの現在の地域と言語の設定で設定された短い日付スタイルに従って書式設定された、日付または式のグレゴリオ暦年を表す整数を返します。
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420711"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="bd013-103">YEAR 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="bd013-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="bd013-104">システムの現在の地域と言語の設定で設定された短い日付スタイルに従って書式設定された、日付または式のグレゴリオ暦年を表す整数を返します。</span><span class="sxs-lookup"><span data-stu-id="bd013-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bd013-105">構文</span><span class="sxs-lookup"><span data-stu-id="bd013-105">Syntax</span></span>

<span data-ttu-id="bd013-106">YEAR(" \*\* *datetime* \*\* "|\*\* *式* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="bd013-106">YEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bd013-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bd013-107">Parameters</span></span>

|<span data-ttu-id="bd013-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="bd013-108">**Name**</span></span>|<span data-ttu-id="bd013-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="bd013-109">**Required/Optional**</span></span>|<span data-ttu-id="bd013-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="bd013-110">**Data Type**</span></span>|<span data-ttu-id="bd013-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="bd013-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bd013-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="bd013-112">_datetime_</span></span> <br/> |<span data-ttu-id="bd013-113">必須</span><span class="sxs-lookup"><span data-stu-id="bd013-113">Required</span></span>  <br/> |<span data-ttu-id="bd013-114">**String**</span><span class="sxs-lookup"><span data-stu-id="bd013-114">**String**</span></span> <br/> | <span data-ttu-id="bd013-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd013-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="bd013-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="bd013-116">_expression_</span></span> <br/> |<span data-ttu-id="bd013-117">必須</span><span class="sxs-lookup"><span data-stu-id="bd013-117">Required</span></span>  <br/> |<span data-ttu-id="bd013-118">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="bd013-118">**Varies**</span></span> <br/> |<span data-ttu-id="bd013-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd013-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="bd013-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="bd013-120">_lcid_</span></span> <br/> |<span data-ttu-id="bd013-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="bd013-121">Optional</span></span>  <br/> |<span data-ttu-id="bd013-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="bd013-122">**Numeric**</span></span> <br/> |<span data-ttu-id="bd013-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="bd013-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bd013-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="bd013-125">Return value</span></span>

<span data-ttu-id="bd013-126">整数</span><span class="sxs-lookup"><span data-stu-id="bd013-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd013-127">注釈</span><span class="sxs-lookup"><span data-stu-id="bd013-127">Remarks</span></span>

<span data-ttu-id="bd013-128">datetime または _式の時刻__コンポーネントは_ 破棄されます。</span><span class="sxs-lookup"><span data-stu-id="bd013-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="bd013-129">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="bd013-129">No rounding is done.</span></span> <span data-ttu-id="bd013-130">datetime  _が見_ つからないか、有効な日付または時刻として解釈できない場合、YEAR はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="bd013-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="bd013-131">YEAR 関数は、結果の整数部分が1899 年 12 月 30 日からの日数を表す式の単一の数値も受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="bd013-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="bd013-132">例 1</span><span class="sxs-lookup"><span data-stu-id="bd013-132">Example 1</span></span>

<span data-ttu-id="bd013-133">YEAR("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="bd013-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="bd013-134">2007 を返します。</span><span class="sxs-lookup"><span data-stu-id="bd013-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bd013-135">例 2</span><span class="sxs-lookup"><span data-stu-id="bd013-135">Example 2</span></span>

<span data-ttu-id="bd013-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="bd013-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="bd013-137">2007 を返します。</span><span class="sxs-lookup"><span data-stu-id="bd013-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bd013-138">例 3</span><span class="sxs-lookup"><span data-stu-id="bd013-138">Example 3</span></span>

<span data-ttu-id="bd013-139">YEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="bd013-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="bd013-140">1997 を返します。</span><span class="sxs-lookup"><span data-stu-id="bd013-140">Returns 1997.</span></span>
  

