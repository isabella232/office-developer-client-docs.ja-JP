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
description: 0 ~ 59、日時または式の秒の部分を表す整数を返します。
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806354"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="3c7a6-103">SECOND 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="3c7a6-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="3c7a6-104">0 ~ 59、_日時_または_式_の秒の部分を表す整数を返します。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3c7a6-105">構文</span><span class="sxs-lookup"><span data-stu-id="3c7a6-105">Syntax</span></span>

<span data-ttu-id="3c7a6-106">2 つ目 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="3c7a6-106">SECOND(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3c7a6-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="3c7a6-107">Parameters</span></span>

|<span data-ttu-id="3c7a6-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="3c7a6-108">**Name**</span></span>|<span data-ttu-id="3c7a6-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3c7a6-109">**Required/Optional**</span></span>|<span data-ttu-id="3c7a6-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3c7a6-110">**Data Type**</span></span>|<span data-ttu-id="3c7a6-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3c7a6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3c7a6-112">_日付時刻_</span><span class="sxs-lookup"><span data-stu-id="3c7a6-112">_datetime_</span></span> <br/> |<span data-ttu-id="3c7a6-113">必須</span><span class="sxs-lookup"><span data-stu-id="3c7a6-113">Required</span></span>  <br/> |<span data-ttu-id="3c7a6-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="3c7a6-114">**String**</span></span> <br/> |<span data-ttu-id="3c7a6-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="3c7a6-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="3c7a6-116">_expression_</span></span> <br/> |<span data-ttu-id="3c7a6-117">必須</span><span class="sxs-lookup"><span data-stu-id="3c7a6-117">Required</span></span>  <br/> |<span data-ttu-id="3c7a6-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="3c7a6-118">**String**</span></span> <br/> | <span data-ttu-id="3c7a6-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="3c7a6-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="3c7a6-120">_lcid_</span></span> <br/> |<span data-ttu-id="3c7a6-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="3c7a6-121">Optional</span></span>  <br/> |<span data-ttu-id="3c7a6-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="3c7a6-122">**Numeric**</span></span> <br/> |<span data-ttu-id="3c7a6-123">現地以外の_datetime_を計算するときに使用されるロケールの識別子です。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="3c7a6-124">ロケール識別子は、システムのヘッダー ファイルに記載されている番号です。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3c7a6-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3c7a6-125">Return value</span></span>

<span data-ttu-id="3c7a6-126">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="3c7a6-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c7a6-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="3c7a6-127">Remarks</span></span>

<span data-ttu-id="3c7a6-128">_日時_または_式_の日付コンポーネントが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="3c7a6-129">丸めは行われません。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-129">No rounding is done.</span></span> <span data-ttu-id="3c7a6-130">_Datetime_が存在しないか、有効な結果に変換することはできません、する場合、この関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="3c7a6-131">2 番目の関数は、結果の小数部分が 1 日午前 0 時からの分数を表す_式_の 1 つの数値値も受け付けます。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="3c7a6-132">例 1</span><span class="sxs-lookup"><span data-stu-id="3c7a6-132">Example 1</span></span>

<span data-ttu-id="3c7a6-133">SECOND("05/30/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="3c7a6-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="3c7a6-134">32 を返します。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3c7a6-135">例 2</span><span class="sxs-lookup"><span data-stu-id="3c7a6-135">Example 2</span></span>

<span data-ttu-id="3c7a6-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span><span class="sxs-lookup"><span data-stu-id="3c7a6-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="3c7a6-137">52 を返します。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3c7a6-138">例 3</span><span class="sxs-lookup"><span data-stu-id="3c7a6-138">Example 3</span></span>

<span data-ttu-id="3c7a6-139">SECOND(0.6337)</span><span class="sxs-lookup"><span data-stu-id="3c7a6-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="3c7a6-140">32 を返します。</span><span class="sxs-lookup"><span data-stu-id="3c7a6-140">Returns 32.</span></span>
  

