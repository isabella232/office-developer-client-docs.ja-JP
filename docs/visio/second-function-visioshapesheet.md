---
title: SECOND 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: datetime または expression の秒の部分を表す 0 ~ 59 の整数を返します。
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332789"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="59e40-103">SECOND 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="59e40-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="59e40-104">_datetime_または_expression_の秒の部分を表す 0 ~ 59 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="59e40-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="59e40-105">構文</span><span class="sxs-lookup"><span data-stu-id="59e40-105">Syntax</span></span>

<span data-ttu-id="59e40-106">2番目 ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="59e40-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="59e40-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="59e40-107">Parameters</span></span>

|<span data-ttu-id="59e40-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="59e40-108">**Name**</span></span>|<span data-ttu-id="59e40-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="59e40-109">**Required/Optional**</span></span>|<span data-ttu-id="59e40-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="59e40-110">**Data Type**</span></span>|<span data-ttu-id="59e40-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="59e40-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="59e40-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="59e40-112">_datetime_</span></span> <br/> |<span data-ttu-id="59e40-113">必須</span><span class="sxs-lookup"><span data-stu-id="59e40-113">Required</span></span>  <br/> |<span data-ttu-id="59e40-114">**String**</span><span class="sxs-lookup"><span data-stu-id="59e40-114">**String**</span></span> <br/> |<span data-ttu-id="59e40-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="59e40-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="59e40-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="59e40-116">_expression_</span></span> <br/> |<span data-ttu-id="59e40-117">必須</span><span class="sxs-lookup"><span data-stu-id="59e40-117">Required</span></span>  <br/> |<span data-ttu-id="59e40-118">**String**</span><span class="sxs-lookup"><span data-stu-id="59e40-118">**String**</span></span> <br/> | <span data-ttu-id="59e40-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="59e40-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="59e40-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="59e40-120">_lcid_</span></span> <br/> |<span data-ttu-id="59e40-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="59e40-121">Optional</span></span>  <br/> |<span data-ttu-id="59e40-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="59e40-122">**Numeric**</span></span> <br/> |<span data-ttu-id="59e40-123">非現地_日付_を評価するときに使用するロケール識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="59e40-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="59e40-124">ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="59e40-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="59e40-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="59e40-125">Return value</span></span>

<span data-ttu-id="59e40-126">整数</span><span class="sxs-lookup"><span data-stu-id="59e40-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59e40-127">解説</span><span class="sxs-lookup"><span data-stu-id="59e40-127">Remarks</span></span>

<span data-ttu-id="59e40-128">_datetime_または_expression_の日付コンポーネントは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="59e40-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="59e40-129">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="59e40-129">No rounding is done.</span></span> <span data-ttu-id="59e40-130">_datetime_が指定されていない場合、または有効な結果に変換できない場合、この関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="59e40-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="59e40-131">2番目の関数では、 _expression_に単一の数値を使用することもできます。この場合、小数点の部分が午前0時からの1日の小数部分を表します。</span><span class="sxs-lookup"><span data-stu-id="59e40-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="59e40-132">例 1</span><span class="sxs-lookup"><span data-stu-id="59e40-132">Example 1</span></span>

<span data-ttu-id="59e40-133">2番目 ("05/30/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="59e40-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="59e40-134">32 を返します。</span><span class="sxs-lookup"><span data-stu-id="59e40-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="59e40-135">例 2</span><span class="sxs-lookup"><span data-stu-id="59e40-135">Example 2</span></span>

<span data-ttu-id="59e40-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span><span class="sxs-lookup"><span data-stu-id="59e40-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="59e40-137">52 を返します。</span><span class="sxs-lookup"><span data-stu-id="59e40-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="59e40-138">例 3</span><span class="sxs-lookup"><span data-stu-id="59e40-138">Example 3</span></span>

<span data-ttu-id="59e40-139">2番目 (0.6337)</span><span class="sxs-lookup"><span data-stu-id="59e40-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="59e40-140">32 を返します。</span><span class="sxs-lookup"><span data-stu-id="59e40-140">Returns 32.</span></span>
  

