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
description: 日時または式の 1 日の時間を表す 0 から 23 の整数を返します。
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805539"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="4a373-103">HOUR 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="4a373-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="4a373-104">_日時_または_式_の 1 日の時間を表す 0 から 23 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="4a373-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4a373-105">構文</span><span class="sxs-lookup"><span data-stu-id="4a373-105">Syntax</span></span>

<span data-ttu-id="4a373-106">時間 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="4a373-106">HOUR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4a373-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4a373-107">Parameters</span></span>

|<span data-ttu-id="4a373-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="4a373-108">**Name**</span></span>|<span data-ttu-id="4a373-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="4a373-109">**Required/Optional**</span></span>|<span data-ttu-id="4a373-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="4a373-110">**Data Type**</span></span>|<span data-ttu-id="4a373-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="4a373-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4a373-112">_日付時刻_</span><span class="sxs-lookup"><span data-stu-id="4a373-112">_datetime_</span></span> <br/> |<span data-ttu-id="4a373-113">必須</span><span class="sxs-lookup"><span data-stu-id="4a373-113">Required</span></span>  <br/> |<span data-ttu-id="4a373-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4a373-114">**String**</span></span> <br/> | <span data-ttu-id="4a373-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a373-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="4a373-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="4a373-116">_expression_</span></span> <br/> |<span data-ttu-id="4a373-117">必須</span><span class="sxs-lookup"><span data-stu-id="4a373-117">Required</span></span>  <br/> |<span data-ttu-id="4a373-118">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="4a373-118">**Varies**</span></span> <br/> |<span data-ttu-id="4a373-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a373-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="4a373-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="4a373-120">_lcid_</span></span> <br/> |<span data-ttu-id="4a373-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="4a373-121">Optional</span></span>  <br/> |<span data-ttu-id="4a373-122">**番号**</span><span class="sxs-lookup"><span data-stu-id="4a373-122">**Number**</span></span> <br/> | <span data-ttu-id="4a373-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="4a373-p101">A locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a373-125">注釈</span><span class="sxs-lookup"><span data-stu-id="4a373-125">Remarks</span></span>

<span data-ttu-id="4a373-126">*Datetime*と*式*の日付コンポーネントが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="4a373-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="4a373-127">丸めは行われません。</span><span class="sxs-lookup"><span data-stu-id="4a373-127">No rounding is done.</span></span> <span data-ttu-id="4a373-128">*Datetime*が存在しないか、有効な結果に変換することはできません、する場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="4a373-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="4a373-129">戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="4a373-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="4a373-130">時間関数では、結果の小数部分が 1 日午前 0 時からの分数を表す*式*の 1 つの数値値も受け付けます。</span><span class="sxs-lookup"><span data-stu-id="4a373-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4a373-131">例 1</span><span class="sxs-lookup"><span data-stu-id="4a373-131">Example 1</span></span>

<span data-ttu-id="4a373-132">HOUR("15:45")</span><span class="sxs-lookup"><span data-stu-id="4a373-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="4a373-133">15 を返します。</span><span class="sxs-lookup"><span data-stu-id="4a373-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4a373-134">例 2</span><span class="sxs-lookup"><span data-stu-id="4a373-134">Example 2</span></span>

<span data-ttu-id="4a373-135">HOUR("May 30, 1997 3:45:24 PM")</span><span class="sxs-lookup"><span data-stu-id="4a373-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="4a373-136">15 を返します。</span><span class="sxs-lookup"><span data-stu-id="4a373-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4a373-137">例 3</span><span class="sxs-lookup"><span data-stu-id="4a373-137">Example 3</span></span>

<span data-ttu-id="4a373-138">HOUR(0.5)</span><span class="sxs-lookup"><span data-stu-id="4a373-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="4a373-139">12 を返します。</span><span class="sxs-lookup"><span data-stu-id="4a373-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="4a373-140">例 4</span><span class="sxs-lookup"><span data-stu-id="4a373-140">Example 4</span></span>

<span data-ttu-id="4a373-141">HOUR("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="4a373-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="4a373-142">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="4a373-142">Returns 0.</span></span>
  

