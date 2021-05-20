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
description: 日付または式の日の時間を表す 0 ~ 23 の整数を返します。
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429636"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="18fa2-103">HOUR 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="18fa2-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="18fa2-104">日付または式の日の時間を表す 0 ~ 23 の  _整数を_ 返  _します_。</span><span class="sxs-lookup"><span data-stu-id="18fa2-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="18fa2-105">構文</span><span class="sxs-lookup"><span data-stu-id="18fa2-105">Syntax</span></span>

<span data-ttu-id="18fa2-106">HOUR(" \*\* *datetime* \*\* "|\*\* *式* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="18fa2-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="18fa2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="18fa2-107">Parameters</span></span>

|<span data-ttu-id="18fa2-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="18fa2-108">**Name**</span></span>|<span data-ttu-id="18fa2-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="18fa2-109">**Required/Optional**</span></span>|<span data-ttu-id="18fa2-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="18fa2-110">**Data Type**</span></span>|<span data-ttu-id="18fa2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="18fa2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="18fa2-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="18fa2-112">_datetime_</span></span> <br/> |<span data-ttu-id="18fa2-113">必須</span><span class="sxs-lookup"><span data-stu-id="18fa2-113">Required</span></span>  <br/> |<span data-ttu-id="18fa2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="18fa2-114">**String**</span></span> <br/> | <span data-ttu-id="18fa2-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="18fa2-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="18fa2-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="18fa2-116">_expression_</span></span> <br/> |<span data-ttu-id="18fa2-117">必須</span><span class="sxs-lookup"><span data-stu-id="18fa2-117">Required</span></span>  <br/> |<span data-ttu-id="18fa2-118">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="18fa2-118">**Varies**</span></span> <br/> |<span data-ttu-id="18fa2-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="18fa2-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="18fa2-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="18fa2-120">_lcid_</span></span> <br/> |<span data-ttu-id="18fa2-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="18fa2-121">Optional</span></span>  <br/> |<span data-ttu-id="18fa2-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="18fa2-122">**Number**</span></span> <br/> | <span data-ttu-id="18fa2-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="18fa2-p101">A locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18fa2-125">注釈</span><span class="sxs-lookup"><span data-stu-id="18fa2-125">Remarks</span></span>

<span data-ttu-id="18fa2-126">datetime および *式の日付\*\*コンポーネントは* 破棄されます。</span><span class="sxs-lookup"><span data-stu-id="18fa2-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="18fa2-127">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="18fa2-127">No rounding is done.</span></span> <span data-ttu-id="18fa2-128">datetime  *が見つからない*  か、有効な結果に変換できない場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="18fa2-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="18fa2-129">戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="18fa2-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="18fa2-130">HOUR 関数は、結果の小数部分が午前 0 時からの 1 日の小数部を表す式の単一の数値も受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="18fa2-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="18fa2-131">例 1</span><span class="sxs-lookup"><span data-stu-id="18fa2-131">Example 1</span></span>

<span data-ttu-id="18fa2-132">HOUR("15:45")</span><span class="sxs-lookup"><span data-stu-id="18fa2-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="18fa2-133">15 を返します。</span><span class="sxs-lookup"><span data-stu-id="18fa2-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="18fa2-134">例 2</span><span class="sxs-lookup"><span data-stu-id="18fa2-134">Example 2</span></span>

<span data-ttu-id="18fa2-135">HOUR("1997 年 5 月 30 日 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="18fa2-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="18fa2-136">15 を返します。</span><span class="sxs-lookup"><span data-stu-id="18fa2-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="18fa2-137">例 3</span><span class="sxs-lookup"><span data-stu-id="18fa2-137">Example 3</span></span>

<span data-ttu-id="18fa2-138">HOUR(0.5)</span><span class="sxs-lookup"><span data-stu-id="18fa2-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="18fa2-139">12 を返します。</span><span class="sxs-lookup"><span data-stu-id="18fa2-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="18fa2-140">例 4</span><span class="sxs-lookup"><span data-stu-id="18fa2-140">Example 4</span></span>

<span data-ttu-id="18fa2-141">HOUR("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="18fa2-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="18fa2-142">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="18fa2-142">Returns 0.</span></span>
  

