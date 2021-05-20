---
title: TIMEVALUE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: システムの地域と言語の設定に基づいて、datetime または式で表される時刻値を返します。
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432325"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="243d9-103">TIMEVALUE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="243d9-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="243d9-104">システムの地域と言語の設定に基づいて、datetime または式で表される時刻値を返します。  </span><span class="sxs-lookup"><span data-stu-id="243d9-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="243d9-105">構文</span><span class="sxs-lookup"><span data-stu-id="243d9-105">Syntax</span></span>

<span data-ttu-id="243d9-106">TIMEVALUE(" \*\* *datetime* \*\* "|\*\* *式* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="243d9-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="243d9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="243d9-107">Parameters</span></span>

|<span data-ttu-id="243d9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="243d9-108">**Name**</span></span>|<span data-ttu-id="243d9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="243d9-109">**Required/Optional**</span></span>|<span data-ttu-id="243d9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="243d9-110">**Data Type**</span></span>|<span data-ttu-id="243d9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="243d9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="243d9-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="243d9-112">_datetime_</span></span> <br/> |<span data-ttu-id="243d9-113">必須</span><span class="sxs-lookup"><span data-stu-id="243d9-113">Required</span></span>  <br/> |<span data-ttu-id="243d9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="243d9-114">**String**</span></span> <br/> | <span data-ttu-id="243d9-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="243d9-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="243d9-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="243d9-116">_expression_</span></span> <br/> |<span data-ttu-id="243d9-117">必須</span><span class="sxs-lookup"><span data-stu-id="243d9-117">Required</span></span>  <br/> |<span data-ttu-id="243d9-118">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="243d9-118">**Varies**</span></span> <br/> | <span data-ttu-id="243d9-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="243d9-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="243d9-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="243d9-120">_lcid_</span></span> <br/> |<span data-ttu-id="243d9-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="243d9-121">Optional</span></span>  <br/> |<span data-ttu-id="243d9-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="243d9-122">**Number**</span></span> <br/> |<span data-ttu-id="243d9-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="243d9-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="243d9-125">注釈</span><span class="sxs-lookup"><span data-stu-id="243d9-125">Remarks</span></span>

<span data-ttu-id="243d9-126">datetime または _式の日付__コンポーネントは_ 破棄されます。</span><span class="sxs-lookup"><span data-stu-id="243d9-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="243d9-127">datetime  _が見_ つからない場合、または有効な結果に変換できない場合、この関数は値を返#VALUE!</span><span class="sxs-lookup"><span data-stu-id="243d9-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="243d9-128">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="243d9-128">error.</span></span> 
  
<span data-ttu-id="243d9-129">TIMEVALUE 関数は、結果の 10進部分が午前 0 時からの 1 日の小数部を表す式の単一の数値も受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="243d9-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="243d9-130">例 1</span><span class="sxs-lookup"><span data-stu-id="243d9-130">Example 1</span></span>

<span data-ttu-id="243d9-131">TIMEVALUE("6:00 AM")</span><span class="sxs-lookup"><span data-stu-id="243d9-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="243d9-132">6:00 AM を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="243d9-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="243d9-133">例 2</span><span class="sxs-lookup"><span data-stu-id="243d9-133">Example 2</span></span>

<span data-ttu-id="243d9-134">TIMEVALUE("14:30")+4 eh.+30 em.</span><span class="sxs-lookup"><span data-stu-id="243d9-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="243d9-135">19:00:00 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="243d9-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="243d9-136">例 3</span><span class="sxs-lookup"><span data-stu-id="243d9-136">Example 3</span></span>

<span data-ttu-id="243d9-137">TIMEVALUE("11 AM, July 1, 1997")</span><span class="sxs-lookup"><span data-stu-id="243d9-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="243d9-138">11:00 AM を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="243d9-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="243d9-139">例 4</span><span class="sxs-lookup"><span data-stu-id="243d9-139">Example 4</span></span>

<span data-ttu-id="243d9-140">TIMEVALUE(0.6337)</span><span class="sxs-lookup"><span data-stu-id="243d9-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="243d9-141">15:12:32 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="243d9-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="243d9-142">例 5</span><span class="sxs-lookup"><span data-stu-id="243d9-142">Example 5</span></span>

<span data-ttu-id="243d9-143">TIMEVALUE("7:89")</span><span class="sxs-lookup"><span data-stu-id="243d9-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="243d9-p103">#VALUE! エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="243d9-p103">Returns a #VALUE! error.</span></span>
  

