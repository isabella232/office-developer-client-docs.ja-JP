---
title: WEEKDAY 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: 日付または式の曜日を表す 1 ~ 7 の整数を返します。
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404807"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="88660-103">WEEKDAY 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="88660-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="88660-104">日付または式の平日を表す 1 ~ 7  _の整数を_ 返  _します_。</span><span class="sxs-lookup"><span data-stu-id="88660-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="88660-105">構文</span><span class="sxs-lookup"><span data-stu-id="88660-105">Syntax</span></span>

<span data-ttu-id="88660-106">WEEKDAY(" \*\* *datetime* \*\* "|\*\* *式* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="88660-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="88660-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="88660-107">Parameters</span></span>

|<span data-ttu-id="88660-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="88660-108">**Name**</span></span>|<span data-ttu-id="88660-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="88660-109">**Required/Optional**</span></span>|<span data-ttu-id="88660-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="88660-110">**Data Type**</span></span>|<span data-ttu-id="88660-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="88660-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="88660-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="88660-112">_datetime_</span></span> <br/> |<span data-ttu-id="88660-113">必須</span><span class="sxs-lookup"><span data-stu-id="88660-113">Required</span></span>  <br/> |<span data-ttu-id="88660-114">**String**</span><span class="sxs-lookup"><span data-stu-id="88660-114">**String**</span></span> <br/> | <span data-ttu-id="88660-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="88660-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="88660-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="88660-116">_expression_</span></span> <br/> |<span data-ttu-id="88660-117">必須</span><span class="sxs-lookup"><span data-stu-id="88660-117">Required</span></span>  <br/> |<span data-ttu-id="88660-118">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="88660-118">**Varies**</span></span> <br/> |<span data-ttu-id="88660-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="88660-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="88660-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="88660-120">_lcid_</span></span> <br/> |<span data-ttu-id="88660-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="88660-121">Optional</span></span>  <br/> |<span data-ttu-id="88660-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="88660-122">**Numeric**</span></span> <br/> |<span data-ttu-id="88660-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="88660-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="88660-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="88660-125">Return value</span></span>

<span data-ttu-id="88660-126">整数</span><span class="sxs-lookup"><span data-stu-id="88660-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88660-127">注釈</span><span class="sxs-lookup"><span data-stu-id="88660-127">Remarks</span></span>

<span data-ttu-id="88660-128">datetime または _式の時刻__コンポーネントは_ 破棄されます。</span><span class="sxs-lookup"><span data-stu-id="88660-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="88660-129">結果は月曜日 (1) から日曜日 (7) に対応します。</span><span class="sxs-lookup"><span data-stu-id="88660-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="88660-130">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="88660-130">No rounding is done.</span></span> <span data-ttu-id="88660-131">datetime  _が見_ つからないか、有効な日付または時刻として解釈できない場合、関数は日付を返#VALUE!</span><span class="sxs-lookup"><span data-stu-id="88660-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="88660-132">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="88660-132">error.</span></span> 
  
<span data-ttu-id="88660-133">また、WEEKDAY 関数は、結果の整数部分が 1899 年 12 月 30 日からの日数を表す式の単一の数値を受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="88660-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="88660-134">例 1</span><span class="sxs-lookup"><span data-stu-id="88660-134">Example 1</span></span>

<span data-ttu-id="88660-135">WEEKDAY("May 30, 1999")</span><span class="sxs-lookup"><span data-stu-id="88660-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="88660-136">7 を返します。</span><span class="sxs-lookup"><span data-stu-id="88660-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="88660-137">例 2</span><span class="sxs-lookup"><span data-stu-id="88660-137">Example 2</span></span>

<span data-ttu-id="88660-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span><span class="sxs-lookup"><span data-stu-id="88660-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="88660-139">2 を返します。</span><span class="sxs-lookup"><span data-stu-id="88660-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="88660-140">例 3</span><span class="sxs-lookup"><span data-stu-id="88660-140">Example 3</span></span>

<span data-ttu-id="88660-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="88660-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="88660-142">4 を返します。</span><span class="sxs-lookup"><span data-stu-id="88660-142">Returns 4.</span></span>
  

