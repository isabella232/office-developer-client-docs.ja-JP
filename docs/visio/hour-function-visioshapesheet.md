---
title: HOUR 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: datetime または expression の日の時間を表す 0 ~ 23 の整数を返します。
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429636"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="a53db-103">HOUR 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a53db-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a53db-104">_datetime_または_expression_の日の時間を表す 0 ~ 23 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="a53db-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a53db-105">構文</span><span class="sxs-lookup"><span data-stu-id="a53db-105">Syntax</span></span>

<span data-ttu-id="a53db-106">時間 ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="a53db-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a53db-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a53db-107">Parameters</span></span>

|<span data-ttu-id="a53db-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="a53db-108">**Name**</span></span>|<span data-ttu-id="a53db-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="a53db-109">**Required/Optional**</span></span>|<span data-ttu-id="a53db-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="a53db-110">**Data Type**</span></span>|<span data-ttu-id="a53db-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a53db-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a53db-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="a53db-112">_datetime_</span></span> <br/> |<span data-ttu-id="a53db-113">必須</span><span class="sxs-lookup"><span data-stu-id="a53db-113">Required</span></span>  <br/> |<span data-ttu-id="a53db-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a53db-114">**String**</span></span> <br/> | <span data-ttu-id="a53db-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="a53db-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a53db-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="a53db-116">_expression_</span></span> <br/> |<span data-ttu-id="a53db-117">必須</span><span class="sxs-lookup"><span data-stu-id="a53db-117">Required</span></span>  <br/> |<span data-ttu-id="a53db-118">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="a53db-118">**Varies**</span></span> <br/> |<span data-ttu-id="a53db-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a53db-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a53db-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="a53db-120">_lcid_</span></span> <br/> |<span data-ttu-id="a53db-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="a53db-121">Optional</span></span>  <br/> |<span data-ttu-id="a53db-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="a53db-122">**Number**</span></span> <br/> | <span data-ttu-id="a53db-123">現地以外の日時を計算するときに使用するロケール識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="a53db-123">A locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="a53db-124">ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="a53db-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a53db-125">注釈</span><span class="sxs-lookup"><span data-stu-id="a53db-125">Remarks</span></span>

<span data-ttu-id="a53db-126">*datetime*および*expression*の日付コンポーネントは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="a53db-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="a53db-127">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="a53db-127">No rounding is done.</span></span> <span data-ttu-id="a53db-128">*datetime*が指定されていない場合、または有効な結果に変換できない場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="a53db-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="a53db-129">戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="a53db-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="a53db-130">HOUR 関数では、 *expression*に単一の数値を使用することもできます。この場合、小数部分には午前0時からの1日の小数部分を表します。</span><span class="sxs-lookup"><span data-stu-id="a53db-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a53db-131">例 1</span><span class="sxs-lookup"><span data-stu-id="a53db-131">Example 1</span></span>

<span data-ttu-id="a53db-132">時間 ("15:45")</span><span class="sxs-lookup"><span data-stu-id="a53db-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="a53db-133">15を返します。</span><span class="sxs-lookup"><span data-stu-id="a53db-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a53db-134">例 2</span><span class="sxs-lookup"><span data-stu-id="a53db-134">Example 2</span></span>

<span data-ttu-id="a53db-135">HOUR ("5 月30日 1997 3:45:24 PM")</span><span class="sxs-lookup"><span data-stu-id="a53db-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="a53db-136">15を返します。</span><span class="sxs-lookup"><span data-stu-id="a53db-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a53db-137">例 3</span><span class="sxs-lookup"><span data-stu-id="a53db-137">Example 3</span></span>

<span data-ttu-id="a53db-138">時間 (0.5)</span><span class="sxs-lookup"><span data-stu-id="a53db-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="a53db-139">12 を返します。</span><span class="sxs-lookup"><span data-stu-id="a53db-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="a53db-140">例 4</span><span class="sxs-lookup"><span data-stu-id="a53db-140">Example 4</span></span>

<span data-ttu-id="a53db-141">時間 ("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="a53db-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="a53db-142">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="a53db-142">Returns 0.</span></span>
  

