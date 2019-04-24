---
title: DATEVALUE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: datetime または expression で表される日付の値を返します。
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360313"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="aa23e-103">DATEVALUE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="aa23e-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="aa23e-104">_datetime_または_expression_で表される日付の値を返します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="aa23e-105">構文</span><span class="sxs-lookup"><span data-stu-id="aa23e-105">Syntax</span></span>

<span data-ttu-id="aa23e-106">DATEVALUE ("\* \* *datetime* \* *" |* **式** \* [, \* \* *lcid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="aa23e-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aa23e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aa23e-107">Parameters</span></span>

|<span data-ttu-id="aa23e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="aa23e-108">**Name**</span></span>|<span data-ttu-id="aa23e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="aa23e-109">**Required/Optional**</span></span>|<span data-ttu-id="aa23e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="aa23e-110">**Data Type**</span></span>|<span data-ttu-id="aa23e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="aa23e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aa23e-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="aa23e-112">_datetime_</span></span> <br/> |<span data-ttu-id="aa23e-113">必須</span><span class="sxs-lookup"><span data-stu-id="aa23e-113">Required</span></span>  <br/> |<span data-ttu-id="aa23e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="aa23e-114">**String**</span></span> <br/> |<span data-ttu-id="aa23e-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="aa23e-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="aa23e-116">_expression_</span></span> <br/> |<span data-ttu-id="aa23e-117">必須</span><span class="sxs-lookup"><span data-stu-id="aa23e-117">Required</span></span>  <br/> |<span data-ttu-id="aa23e-118">**String**</span><span class="sxs-lookup"><span data-stu-id="aa23e-118">**String**</span></span> <br/> |<span data-ttu-id="aa23e-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="aa23e-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="aa23e-120">_lcid_</span></span> <br/> |<span data-ttu-id="aa23e-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="aa23e-121">Optional</span></span>  <br/> |<span data-ttu-id="aa23e-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="aa23e-122">**Number**</span></span> <br/> |<span data-ttu-id="aa23e-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="aa23e-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aa23e-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="aa23e-125">Return value</span></span>

<span data-ttu-id="aa23e-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="aa23e-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa23e-127">解説</span><span class="sxs-lookup"><span data-stu-id="aa23e-127">Remarks</span></span>

<span data-ttu-id="aa23e-128">*datetime*または*expression*の時刻コンポーネントは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="aa23e-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="aa23e-129">*datetime*が指定されていない場合、または有効な結果に変換できない場合は、DATEVALUE は #VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="aa23e-130">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-130">error.</span></span> 
  
<span data-ttu-id="aa23e-131">戻り値は、システムの現在の [地域の設定] に設定されている短い形式の日付で表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa23e-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="aa23e-132">また、DATEVALUE 関数では、 *expression*に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="aa23e-133">例 1</span><span class="sxs-lookup"><span data-stu-id="aa23e-133">Example 1</span></span>

<span data-ttu-id="aa23e-134">DATEVALUE(NOW( ))+5 ed.</span><span class="sxs-lookup"><span data-stu-id="aa23e-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="aa23e-135">現在から 5 日後の日付を返します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="aa23e-136">例 2</span><span class="sxs-lookup"><span data-stu-id="aa23e-136">Example 2</span></span>

<span data-ttu-id="aa23e-137">DATEVALUE ("7/19/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="aa23e-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="aa23e-138">日付を返します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="aa23e-139">例 3</span><span class="sxs-lookup"><span data-stu-id="aa23e-139">Example 3</span></span>

<span data-ttu-id="aa23e-140">DATEVALUE("May 33, 1997")</span><span class="sxs-lookup"><span data-stu-id="aa23e-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="aa23e-p103">#VALUE! エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-p103">Returns a #VALUE! error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="aa23e-143">例 4</span><span class="sxs-lookup"><span data-stu-id="aa23e-143">Example 4</span></span>

<span data-ttu-id="aa23e-144">DATEVALUE (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="aa23e-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="aa23e-145">5/30/1997 を返します。</span><span class="sxs-lookup"><span data-stu-id="aa23e-145">Returns 5/30/1997.</span></span>
  

