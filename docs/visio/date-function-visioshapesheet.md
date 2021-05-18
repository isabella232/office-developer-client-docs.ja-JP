---
title: DATE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: システムの地域情報の短い日付スタイルに従って書式設定された年、月、および日で表される日付を設定。 年、月、および日の値は、グレゴリオ暦を反映します。
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360334"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="7f600-104">DATE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="7f600-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="7f600-105">システムの地域情報の短い日付スタイルに従って書式設定された年、月、および日で表される日付を設定。</span><span class="sxs-lookup"><span data-stu-id="7f600-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="7f600-106">年、月 *、\*\*および* 日の値 *は*、グレゴリオ暦を反映します。</span><span class="sxs-lookup"><span data-stu-id="7f600-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7f600-107">構文</span><span class="sxs-lookup"><span data-stu-id="7f600-107">Syntax</span></span>

<span data-ttu-id="7f600-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span><span class="sxs-lookup"><span data-stu-id="7f600-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7f600-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7f600-109">Parameters</span></span>

|<span data-ttu-id="7f600-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="7f600-110">**Name**</span></span>|<span data-ttu-id="7f600-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="7f600-111">**Required/Optional**</span></span>|<span data-ttu-id="7f600-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="7f600-112">**Data Type**</span></span>|<span data-ttu-id="7f600-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="7f600-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7f600-114">_year_</span><span class="sxs-lookup"><span data-stu-id="7f600-114">_year_</span></span> <br/> |<span data-ttu-id="7f600-115">必須</span><span class="sxs-lookup"><span data-stu-id="7f600-115">Required</span></span>  <br/> |<span data-ttu-id="7f600-116">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="7f600-116">**Integer**</span></span> <br/> |<span data-ttu-id="7f600-117">年を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f600-117">The year.</span></span>  <br/> |
| <span data-ttu-id="7f600-118">_month_</span><span class="sxs-lookup"><span data-stu-id="7f600-118">_month_</span></span> <br/> |<span data-ttu-id="7f600-119">必須</span><span class="sxs-lookup"><span data-stu-id="7f600-119">Required</span></span>  <br/> |<span data-ttu-id="7f600-120">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="7f600-120">**Integer**</span></span> <br/> |<span data-ttu-id="7f600-121">月を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f600-121">The month.</span></span>  <br/> |
| <span data-ttu-id="7f600-122">_day_</span><span class="sxs-lookup"><span data-stu-id="7f600-122">_day_</span></span> <br/> |<span data-ttu-id="7f600-123">必須</span><span class="sxs-lookup"><span data-stu-id="7f600-123">Required</span></span>  <br/> |<span data-ttu-id="7f600-124">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="7f600-124">**Integer**</span></span> <br/> |<span data-ttu-id="7f600-125">日を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f600-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="7f600-126">例 1</span><span class="sxs-lookup"><span data-stu-id="7f600-126">Example 1</span></span>

<span data-ttu-id="7f600-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="7f600-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="7f600-128">07.06.99 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="7f600-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7f600-129">例 2</span><span class="sxs-lookup"><span data-stu-id="7f600-129">Example 2</span></span>

<span data-ttu-id="7f600-130">DATE(1999,6,7) + 4 ed.</span><span class="sxs-lookup"><span data-stu-id="7f600-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="7f600-131">6/11/1999 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="7f600-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7f600-132">例 3</span><span class="sxs-lookup"><span data-stu-id="7f600-132">Example 3</span></span>

<span data-ttu-id="7f600-133">FORMAT(DATE(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="7f600-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="7f600-134">1999 年 10 月 14 日、火曜日を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="7f600-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

