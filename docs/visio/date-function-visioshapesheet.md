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
description: システムの地域の設定で短い日付形式に従って、年、月、および日で表される日付を返します。 年、月、および日の値は、グレゴリオ暦を反映しています。
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360334"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="66c53-104">DATE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="66c53-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="66c53-105">システムの地域の設定で短い日付形式に従って、*年、月、* および*日*で表される日付を返します。</span><span class="sxs-lookup"><span data-stu-id="66c53-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="66c53-106">*年*、*月*、および*日*の値は、グレゴリオ暦を反映しています。</span><span class="sxs-lookup"><span data-stu-id="66c53-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="66c53-107">構文</span><span class="sxs-lookup"><span data-stu-id="66c53-107">Syntax</span></span>

<span data-ttu-id="66c53-108">DATE (\* **年** *、* **月** *、* **日** \*)</span><span class="sxs-lookup"><span data-stu-id="66c53-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="66c53-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="66c53-109">Parameters</span></span>

|<span data-ttu-id="66c53-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="66c53-110">**Name**</span></span>|<span data-ttu-id="66c53-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="66c53-111">**Required/Optional**</span></span>|<span data-ttu-id="66c53-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="66c53-112">**Data Type**</span></span>|<span data-ttu-id="66c53-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="66c53-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="66c53-114">_year_</span><span class="sxs-lookup"><span data-stu-id="66c53-114">_year_</span></span> <br/> |<span data-ttu-id="66c53-115">必須</span><span class="sxs-lookup"><span data-stu-id="66c53-115">Required</span></span>  <br/> |<span data-ttu-id="66c53-116">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="66c53-116">**Integer**</span></span> <br/> |<span data-ttu-id="66c53-117">年を指定します。</span><span class="sxs-lookup"><span data-stu-id="66c53-117">The year.</span></span>  <br/> |
| <span data-ttu-id="66c53-118">_month_</span><span class="sxs-lookup"><span data-stu-id="66c53-118">_month_</span></span> <br/> |<span data-ttu-id="66c53-119">必須</span><span class="sxs-lookup"><span data-stu-id="66c53-119">Required</span></span>  <br/> |<span data-ttu-id="66c53-120">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="66c53-120">**Integer**</span></span> <br/> |<span data-ttu-id="66c53-121">月を指定します。</span><span class="sxs-lookup"><span data-stu-id="66c53-121">The month.</span></span>  <br/> |
| <span data-ttu-id="66c53-122">_day_</span><span class="sxs-lookup"><span data-stu-id="66c53-122">_day_</span></span> <br/> |<span data-ttu-id="66c53-123">必須</span><span class="sxs-lookup"><span data-stu-id="66c53-123">Required</span></span>  <br/> |<span data-ttu-id="66c53-124">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="66c53-124">**Integer**</span></span> <br/> |<span data-ttu-id="66c53-125">日を指定します。</span><span class="sxs-lookup"><span data-stu-id="66c53-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="66c53-126">例 1</span><span class="sxs-lookup"><span data-stu-id="66c53-126">Example 1</span></span>

<span data-ttu-id="66c53-127">DATE (1999、6、7)</span><span class="sxs-lookup"><span data-stu-id="66c53-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="66c53-128">07.06.99 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="66c53-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="66c53-129">例 2</span><span class="sxs-lookup"><span data-stu-id="66c53-129">Example 2</span></span>

<span data-ttu-id="66c53-130">DATE(1999,6,7) + 4 ed.</span><span class="sxs-lookup"><span data-stu-id="66c53-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="66c53-131">6/11/1999 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="66c53-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="66c53-132">例 3</span><span class="sxs-lookup"><span data-stu-id="66c53-132">Example 3</span></span>

<span data-ttu-id="66c53-133">形式 (DATE (1999、10、14)、"C")</span><span class="sxs-lookup"><span data-stu-id="66c53-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="66c53-134">1999 年 10 月 14 日、火曜日を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="66c53-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

