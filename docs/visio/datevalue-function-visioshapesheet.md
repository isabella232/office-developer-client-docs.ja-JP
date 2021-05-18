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
description: datetime または式で表される日付値を返します。
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360313"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="c0496-103">DATEVALUE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c0496-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c0496-104">datetime または式で表される日付  _値を_ 返  _します_。</span><span class="sxs-lookup"><span data-stu-id="c0496-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c0496-105">構文</span><span class="sxs-lookup"><span data-stu-id="c0496-105">Syntax</span></span>

<span data-ttu-id="c0496-106">DATEVALUE(" \*\* *datetime* \*\* "|\*\* *式* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="c0496-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0496-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c0496-107">Parameters</span></span>

|<span data-ttu-id="c0496-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="c0496-108">**Name**</span></span>|<span data-ttu-id="c0496-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c0496-109">**Required/Optional**</span></span>|<span data-ttu-id="c0496-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c0496-110">**Data Type**</span></span>|<span data-ttu-id="c0496-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c0496-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0496-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="c0496-112">_datetime_</span></span> <br/> |<span data-ttu-id="c0496-113">必須</span><span class="sxs-lookup"><span data-stu-id="c0496-113">Required</span></span>  <br/> |<span data-ttu-id="c0496-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c0496-114">**String**</span></span> <br/> |<span data-ttu-id="c0496-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0496-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="c0496-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="c0496-116">_expression_</span></span> <br/> |<span data-ttu-id="c0496-117">必須</span><span class="sxs-lookup"><span data-stu-id="c0496-117">Required</span></span>  <br/> |<span data-ttu-id="c0496-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c0496-118">**String**</span></span> <br/> |<span data-ttu-id="c0496-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0496-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="c0496-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="c0496-120">_lcid_</span></span> <br/> |<span data-ttu-id="c0496-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="c0496-121">Optional</span></span>  <br/> |<span data-ttu-id="c0496-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="c0496-122">**Number**</span></span> <br/> |<span data-ttu-id="c0496-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="c0496-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c0496-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="c0496-125">Return value</span></span>

<span data-ttu-id="c0496-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="c0496-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0496-127">注釈</span><span class="sxs-lookup"><span data-stu-id="c0496-127">Remarks</span></span>

<span data-ttu-id="c0496-128">datetime または  *式内の*  任意の  *時刻コンポーネント*  は破棄されます。</span><span class="sxs-lookup"><span data-stu-id="c0496-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="c0496-129">datetime  *が見*  つからないか、有効な結果に変換できない場合、DATEVALUE は値を返#VALUE!</span><span class="sxs-lookup"><span data-stu-id="c0496-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="c0496-130">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="c0496-130">error.</span></span> 
  
<span data-ttu-id="c0496-131">戻り値は、システムの現在の [地域の設定] に設定されている短い形式の日付で表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0496-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="c0496-132">DATEVALUE 関数は、結果の整数部分が1899 年 12 月 30 日からの日数を表す式の 1 つの数値値も受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="c0496-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c0496-133">例 1</span><span class="sxs-lookup"><span data-stu-id="c0496-133">Example 1</span></span>

<span data-ttu-id="c0496-134">DATEVALUE(NOW( ))+5 ed.</span><span class="sxs-lookup"><span data-stu-id="c0496-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="c0496-135">現在から 5 日後の日付を返します。</span><span class="sxs-lookup"><span data-stu-id="c0496-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c0496-136">例 2</span><span class="sxs-lookup"><span data-stu-id="c0496-136">Example 2</span></span>

<span data-ttu-id="c0496-137">DATEVALUE("7/19/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="c0496-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="c0496-138">日付を返します。</span><span class="sxs-lookup"><span data-stu-id="c0496-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c0496-139">例 3</span><span class="sxs-lookup"><span data-stu-id="c0496-139">Example 3</span></span>

<span data-ttu-id="c0496-140">DATEVALUE("May 33, 1997")</span><span class="sxs-lookup"><span data-stu-id="c0496-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="c0496-p103">#VALUE! エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="c0496-p103">Returns a #VALUE! error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="c0496-143">例 4</span><span class="sxs-lookup"><span data-stu-id="c0496-143">Example 4</span></span>

<span data-ttu-id="c0496-144">DATEVALUE(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="c0496-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="c0496-145">5/30/1997 を返します。</span><span class="sxs-lookup"><span data-stu-id="c0496-145">Returns 5/30/1997.</span></span>
  

