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
description: datetime または式の分のコンポーネントを表す 0 ~ 59 の整数を返します。
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436567"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="ed12c-103">MINUTE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="ed12c-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="ed12c-104">datetime または式の分のコンポーネントを表す 0 ~ 59 の  *整数を*  返  *します*  。</span><span class="sxs-lookup"><span data-stu-id="ed12c-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ed12c-105">構文</span><span class="sxs-lookup"><span data-stu-id="ed12c-105">Syntax</span></span>

<span data-ttu-id="ed12c-106">MINUTE(" *datetime*  "|  *式*  [,  *lcid*  ])</span><span class="sxs-lookup"><span data-stu-id="ed12c-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ed12c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ed12c-107">Parameters</span></span>

|<span data-ttu-id="ed12c-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="ed12c-108">**Name**</span></span>|<span data-ttu-id="ed12c-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ed12c-109">**Required/Optional**</span></span>|<span data-ttu-id="ed12c-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ed12c-110">**Data Type**</span></span>|<span data-ttu-id="ed12c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="ed12c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ed12c-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="ed12c-112">_datetime_</span></span> <br/> |<span data-ttu-id="ed12c-113">必須</span><span class="sxs-lookup"><span data-stu-id="ed12c-113">Required</span></span>  <br/> |<span data-ttu-id="ed12c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ed12c-114">**String**</span></span> <br/> |<span data-ttu-id="ed12c-115">日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="ed12c-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="ed12c-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="ed12c-116">_expression_</span></span> <br/> |<span data-ttu-id="ed12c-117">必須</span><span class="sxs-lookup"><span data-stu-id="ed12c-117">Required</span></span>  <br/> |<span data-ttu-id="ed12c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ed12c-118">**String**</span></span> <br/> | <span data-ttu-id="ed12c-119">日付および時刻を算出する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="ed12c-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="ed12c-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="ed12c-120">_lcid_</span></span> <br/> |<span data-ttu-id="ed12c-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="ed12c-121">Optional</span></span>  <br/> |<span data-ttu-id="ed12c-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="ed12c-122">**Number**</span></span> <br/> |<span data-ttu-id="ed12c-p101">現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。</span><span class="sxs-lookup"><span data-stu-id="ed12c-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ed12c-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="ed12c-125">Return value</span></span>

<span data-ttu-id="ed12c-126">整数</span><span class="sxs-lookup"><span data-stu-id="ed12c-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed12c-127">注釈</span><span class="sxs-lookup"><span data-stu-id="ed12c-127">Remarks</span></span>

<span data-ttu-id="ed12c-128">datetime および _式の日付__コンポーネントは_ 破棄されます。</span><span class="sxs-lookup"><span data-stu-id="ed12c-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="ed12c-129">数値は四捨五入されません。</span><span class="sxs-lookup"><span data-stu-id="ed12c-129">No rounding is done.</span></span> <span data-ttu-id="ed12c-130">datetime  _が見_ つからないか、有効な結果に変換できない場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="ed12c-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="ed12c-131">戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="ed12c-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="ed12c-132">MINUTE 関数は、10 進数の部分が午前 0 時からの 1 日の端数を表す式の単一の数値も受け取る。</span><span class="sxs-lookup"><span data-stu-id="ed12c-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ed12c-133">例 1</span><span class="sxs-lookup"><span data-stu-id="ed12c-133">Example 1</span></span>

<span data-ttu-id="ed12c-134">MINUTE("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="ed12c-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="ed12c-135">45 を返します。</span><span class="sxs-lookup"><span data-stu-id="ed12c-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ed12c-136">例 2</span><span class="sxs-lookup"><span data-stu-id="ed12c-136">Example 2</span></span>

<span data-ttu-id="ed12c-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span><span class="sxs-lookup"><span data-stu-id="ed12c-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="ed12c-138">13 を返します。</span><span class="sxs-lookup"><span data-stu-id="ed12c-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ed12c-139">例 3</span><span class="sxs-lookup"><span data-stu-id="ed12c-139">Example 3</span></span>

<span data-ttu-id="ed12c-140">MINUTE(0.575)</span><span class="sxs-lookup"><span data-stu-id="ed12c-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="ed12c-141">48 を返します。</span><span class="sxs-lookup"><span data-stu-id="ed12c-141">Returns 48.</span></span>
  

