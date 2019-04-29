---
title: MONTH 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: 月を表す1から12までの整数を返します。
ms.openlocfilehash: 71ecc7992839c871780e9b703377db37279246e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431975"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="ad18d-103">MONTH 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="ad18d-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="ad18d-104">月を表す1から12までの整数を返します。</span><span class="sxs-lookup"><span data-stu-id="ad18d-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ad18d-105">構文</span><span class="sxs-lookup"><span data-stu-id="ad18d-105">Syntax</span></span>

<span data-ttu-id="ad18d-106">MONTH ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="ad18d-106">MONTH(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ad18d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ad18d-107">Parameters</span></span>

|<span data-ttu-id="ad18d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="ad18d-108">**Name**</span></span>|<span data-ttu-id="ad18d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ad18d-109">**Required/Optional**</span></span>|<span data-ttu-id="ad18d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ad18d-110">**Data Type**</span></span>|<span data-ttu-id="ad18d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad18d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ad18d-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="ad18d-112">_datetime_</span></span> <br/> |<span data-ttu-id="ad18d-113">必須</span><span class="sxs-lookup"><span data-stu-id="ad18d-113">Required</span></span>  <br/> |<span data-ttu-id="ad18d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ad18d-114">**String**</span></span> <br/> |<span data-ttu-id="ad18d-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad18d-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="ad18d-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="ad18d-116">_expression_</span></span> <br/> |<span data-ttu-id="ad18d-117">必須</span><span class="sxs-lookup"><span data-stu-id="ad18d-117">Required</span></span>  <br/> |<span data-ttu-id="ad18d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ad18d-118">**String**</span></span> <br/> | <span data-ttu-id="ad18d-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad18d-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="ad18d-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="ad18d-120">_lcid_</span></span> <br/> |<span data-ttu-id="ad18d-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="ad18d-121">Optional</span></span>  <br/> |<span data-ttu-id="ad18d-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="ad18d-122">**Number**</span></span> <br/> |<span data-ttu-id="ad18d-123">現地以外の日時を計算するときに使用するロケール識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad18d-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="ad18d-124">ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="ad18d-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ad18d-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="ad18d-125">Return value</span></span>

<span data-ttu-id="ad18d-126">整数</span><span class="sxs-lookup"><span data-stu-id="ad18d-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad18d-127">注釈</span><span class="sxs-lookup"><span data-stu-id="ad18d-127">Remarks</span></span>

<span data-ttu-id="ad18d-128">_datetime_または_expression_の時刻コンポーネントは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="ad18d-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="ad18d-p102">数値は四捨五入されません。入力文字列が指定されていない場合、または有効な結果に変換できない場合、MONTH 関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="ad18d-p102">No rounding is done. If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="ad18d-131">戻り値は、システムの現在の [地域別設定] に設定されている短い形式の日付で書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="ad18d-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="ad18d-132">MONTH 関数では、 _expression_に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad18d-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ad18d-133">例 1</span><span class="sxs-lookup"><span data-stu-id="ad18d-133">Example 1</span></span>

<span data-ttu-id="ad18d-134">MONTH("May 30, 1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="ad18d-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="ad18d-135">5 を返します。</span><span class="sxs-lookup"><span data-stu-id="ad18d-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ad18d-136">例 2</span><span class="sxs-lookup"><span data-stu-id="ad18d-136">Example 2</span></span>

<span data-ttu-id="ad18d-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="ad18d-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="ad18d-138">6 を返します。</span><span class="sxs-lookup"><span data-stu-id="ad18d-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ad18d-139">例 3</span><span class="sxs-lookup"><span data-stu-id="ad18d-139">Example 3</span></span>

<span data-ttu-id="ad18d-140">月 (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="ad18d-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="ad18d-141">5 を返します。</span><span class="sxs-lookup"><span data-stu-id="ad18d-141">Returns 5.</span></span>
  

