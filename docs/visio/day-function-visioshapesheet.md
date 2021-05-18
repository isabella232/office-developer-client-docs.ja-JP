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
description: 日付または式の日を表す 1 ~ 31 の整数を返します。 DAY 関数はグレゴリオ暦を使用します。
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360298"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="fe73b-104">DAY 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fe73b-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fe73b-105">日付または式の日を表す 1 ~ 31  _の整数を_ 返  _します_。</span><span class="sxs-lookup"><span data-stu-id="fe73b-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="fe73b-106">DAY 関数はグレゴリオ暦を使用します。</span><span class="sxs-lookup"><span data-stu-id="fe73b-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fe73b-107">構文</span><span class="sxs-lookup"><span data-stu-id="fe73b-107">Syntax</span></span>

<span data-ttu-id="fe73b-108">DAY(" \*\* *datetime* \*\* "|\*\* *式* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="fe73b-108">DAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fe73b-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fe73b-109">Parameters</span></span>

|<span data-ttu-id="fe73b-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="fe73b-110">**Name**</span></span>|<span data-ttu-id="fe73b-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="fe73b-111">**Required/Optional**</span></span>|<span data-ttu-id="fe73b-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="fe73b-112">**Data Type**</span></span>|<span data-ttu-id="fe73b-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="fe73b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fe73b-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="fe73b-114">_datetime_</span></span> <br/> |<span data-ttu-id="fe73b-115">必須</span><span class="sxs-lookup"><span data-stu-id="fe73b-115">Required</span></span>  <br/> |<span data-ttu-id="fe73b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="fe73b-116">**String**</span></span> <br/> |<span data-ttu-id="fe73b-117">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="fe73b-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="fe73b-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="fe73b-118">_expression_</span></span> <br/> |<span data-ttu-id="fe73b-119">必須</span><span class="sxs-lookup"><span data-stu-id="fe73b-119">Required</span></span>  <br/> |<span data-ttu-id="fe73b-120">**String**</span><span class="sxs-lookup"><span data-stu-id="fe73b-120">**String**</span></span> <br/> |<span data-ttu-id="fe73b-121">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="fe73b-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="fe73b-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="fe73b-122">_lcid_</span></span> <br/> |<span data-ttu-id="fe73b-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="fe73b-123">Optional</span></span>  <br/> |<span data-ttu-id="fe73b-124">**数値**</span><span class="sxs-lookup"><span data-stu-id="fe73b-124">**Number**</span></span> <br/> |<span data-ttu-id="fe73b-p103">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="fe73b-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fe73b-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="fe73b-127">Return value</span></span>

<span data-ttu-id="fe73b-128">整数</span><span class="sxs-lookup"><span data-stu-id="fe73b-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe73b-129">注釈</span><span class="sxs-lookup"><span data-stu-id="fe73b-129">Remarks</span></span>

<span data-ttu-id="fe73b-130">datetime または  _式内の_ 任意の  _時刻コンポーネント_ は破棄されます。</span><span class="sxs-lookup"><span data-stu-id="fe73b-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="fe73b-131">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="fe73b-131">No rounding is done.</span></span> <span data-ttu-id="fe73b-132">datetime  _が見_ つからないか、有効な結果に変換できない場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="fe73b-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="fe73b-133">DAY 関数は、結果の整数部分が1899 年 12 月 30 日からの日数を表す式の単一の数値も受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="fe73b-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fe73b-134">例 1</span><span class="sxs-lookup"><span data-stu-id="fe73b-134">Example 1</span></span>

<span data-ttu-id="fe73b-135">DAY("May 30, 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="fe73b-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="fe73b-136">30 を返します。</span><span class="sxs-lookup"><span data-stu-id="fe73b-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fe73b-137">例 2</span><span class="sxs-lookup"><span data-stu-id="fe73b-137">Example 2</span></span>

<span data-ttu-id="fe73b-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="fe73b-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="fe73b-139">6 を返します。</span><span class="sxs-lookup"><span data-stu-id="fe73b-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fe73b-140">例 3</span><span class="sxs-lookup"><span data-stu-id="fe73b-140">Example 3</span></span>

<span data-ttu-id="fe73b-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="fe73b-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="fe73b-142">30 を返します。</span><span class="sxs-lookup"><span data-stu-id="fe73b-142">Returns 30.</span></span>
  

