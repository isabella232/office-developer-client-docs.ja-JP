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
description: 0 から 59 日時または式の分コンポーネントを表す整数を返します。
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805905"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="97f59-103">MINUTE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="97f59-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="97f59-104">0 から 59*日時*または*式*の分コンポーネントを表す整数を返します。</span><span class="sxs-lookup"><span data-stu-id="97f59-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="97f59-105">構文</span><span class="sxs-lookup"><span data-stu-id="97f59-105">Syntax</span></span>

<span data-ttu-id="97f59-106">分 (" *datetime* "| *式* [、 *lcid* ])</span><span class="sxs-lookup"><span data-stu-id="97f59-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="97f59-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="97f59-107">Parameters</span></span>

|<span data-ttu-id="97f59-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="97f59-108">**Name**</span></span>|<span data-ttu-id="97f59-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="97f59-109">**Required/Optional**</span></span>|<span data-ttu-id="97f59-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="97f59-110">**Data Type**</span></span>|<span data-ttu-id="97f59-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="97f59-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="97f59-112">_日付時刻_</span><span class="sxs-lookup"><span data-stu-id="97f59-112">_datetime_</span></span> <br/> |<span data-ttu-id="97f59-113">必須</span><span class="sxs-lookup"><span data-stu-id="97f59-113">Required</span></span>  <br/> |<span data-ttu-id="97f59-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="97f59-114">**String**</span></span> <br/> |<span data-ttu-id="97f59-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="97f59-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="97f59-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="97f59-116">_expression_</span></span> <br/> |<span data-ttu-id="97f59-117">必須</span><span class="sxs-lookup"><span data-stu-id="97f59-117">Required</span></span>  <br/> |<span data-ttu-id="97f59-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="97f59-118">**String**</span></span> <br/> | <span data-ttu-id="97f59-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="97f59-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="97f59-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="97f59-120">_lcid_</span></span> <br/> |<span data-ttu-id="97f59-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="97f59-121">Optional</span></span>  <br/> |<span data-ttu-id="97f59-122">**番号**</span><span class="sxs-lookup"><span data-stu-id="97f59-122">**Number**</span></span> <br/> |<span data-ttu-id="97f59-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="97f59-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="97f59-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="97f59-125">Return value</span></span>

<span data-ttu-id="97f59-126">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="97f59-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97f59-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="97f59-127">Remarks</span></span>

<span data-ttu-id="97f59-128">_Datetime_と_式_の日付コンポーネントが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="97f59-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="97f59-129">丸めは行われません。</span><span class="sxs-lookup"><span data-stu-id="97f59-129">No rounding is done.</span></span> <span data-ttu-id="97f59-130">_Datetime_が存在しないか、有効な結果に変換することはできません、する場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="97f59-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="97f59-131">戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="97f59-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="97f59-132">MINUTE 関数では、小数部分が 1 日午前 0 時からの分数を表す_式_の 1 つの数値値も受け付けます。</span><span class="sxs-lookup"><span data-stu-id="97f59-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="97f59-133">例 1</span><span class="sxs-lookup"><span data-stu-id="97f59-133">Example 1</span></span>

<span data-ttu-id="97f59-134">MINUTE("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="97f59-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="97f59-135">45 を返します。</span><span class="sxs-lookup"><span data-stu-id="97f59-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="97f59-136">例 2</span><span class="sxs-lookup"><span data-stu-id="97f59-136">Example 2</span></span>

<span data-ttu-id="97f59-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span><span class="sxs-lookup"><span data-stu-id="97f59-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="97f59-138">13 を返します。</span><span class="sxs-lookup"><span data-stu-id="97f59-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="97f59-139">例 3</span><span class="sxs-lookup"><span data-stu-id="97f59-139">Example 3</span></span>

<span data-ttu-id="97f59-140">MINUTE(0.575)</span><span class="sxs-lookup"><span data-stu-id="97f59-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="97f59-141">48 を返します。</span><span class="sxs-lookup"><span data-stu-id="97f59-141">Returns 48.</span></span>
  

