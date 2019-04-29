---
title: MINUTE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: datetime または expression の分の部分を表す 0 ~ 59 の整数を返します。
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436567"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="9946a-103">MINUTE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="9946a-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="9946a-104">*datetime*または*expression*の分の部分を表す 0 ~ 59 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="9946a-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9946a-105">構文</span><span class="sxs-lookup"><span data-stu-id="9946a-105">Syntax</span></span>

<span data-ttu-id="9946a-106">分 (" *datetime* " | *式* [, *lcid* ])</span><span class="sxs-lookup"><span data-stu-id="9946a-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9946a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9946a-107">Parameters</span></span>

|<span data-ttu-id="9946a-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="9946a-108">**Name**</span></span>|<span data-ttu-id="9946a-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="9946a-109">**Required/Optional**</span></span>|<span data-ttu-id="9946a-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="9946a-110">**Data Type**</span></span>|<span data-ttu-id="9946a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="9946a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9946a-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="9946a-112">_datetime_</span></span> <br/> |<span data-ttu-id="9946a-113">必須</span><span class="sxs-lookup"><span data-stu-id="9946a-113">Required</span></span>  <br/> |<span data-ttu-id="9946a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9946a-114">**String**</span></span> <br/> |<span data-ttu-id="9946a-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="9946a-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="9946a-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="9946a-116">_expression_</span></span> <br/> |<span data-ttu-id="9946a-117">必須</span><span class="sxs-lookup"><span data-stu-id="9946a-117">Required</span></span>  <br/> |<span data-ttu-id="9946a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9946a-118">**String**</span></span> <br/> | <span data-ttu-id="9946a-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="9946a-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="9946a-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="9946a-120">_lcid_</span></span> <br/> |<span data-ttu-id="9946a-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="9946a-121">Optional</span></span>  <br/> |<span data-ttu-id="9946a-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="9946a-122">**Number**</span></span> <br/> |<span data-ttu-id="9946a-123">現地以外の日時を計算するときに使用するロケール識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="9946a-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="9946a-124">ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="9946a-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9946a-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="9946a-125">Return value</span></span>

<span data-ttu-id="9946a-126">整数</span><span class="sxs-lookup"><span data-stu-id="9946a-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9946a-127">注釈</span><span class="sxs-lookup"><span data-stu-id="9946a-127">Remarks</span></span>

<span data-ttu-id="9946a-128">_datetime_および_expression_の日付コンポーネントは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="9946a-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="9946a-129">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="9946a-129">No rounding is done.</span></span> <span data-ttu-id="9946a-130">_datetime_が指定されていない場合、または有効な結果に変換できない場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="9946a-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="9946a-131">戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="9946a-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="9946a-132">MINUTE 関数では、 _expression_に単一の数値を使用することもできます。この場合、小数部分には午前0時からの1日の小数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9946a-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="9946a-133">例 1</span><span class="sxs-lookup"><span data-stu-id="9946a-133">Example 1</span></span>

<span data-ttu-id="9946a-134">分 ("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="9946a-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="9946a-135">45 を返します。</span><span class="sxs-lookup"><span data-stu-id="9946a-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9946a-136">例 2</span><span class="sxs-lookup"><span data-stu-id="9946a-136">Example 2</span></span>

<span data-ttu-id="9946a-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span><span class="sxs-lookup"><span data-stu-id="9946a-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="9946a-138">13 を返します。</span><span class="sxs-lookup"><span data-stu-id="9946a-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="9946a-139">例 3</span><span class="sxs-lookup"><span data-stu-id="9946a-139">Example 3</span></span>

<span data-ttu-id="9946a-140">分 (0.575)</span><span class="sxs-lookup"><span data-stu-id="9946a-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="9946a-141">48 を返します。</span><span class="sxs-lookup"><span data-stu-id="9946a-141">Returns 48.</span></span>
  

