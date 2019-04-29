---
title: TIME 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: hour、minute、および second で表される時間を返します。
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414474"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="a50d4-103">TIME 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a50d4-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a50d4-104">_hour_、 _minute_、および_second_で表される時間を返します。</span><span class="sxs-lookup"><span data-stu-id="a50d4-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a50d4-105">構文</span><span class="sxs-lookup"><span data-stu-id="a50d4-105">Syntax</span></span>

<span data-ttu-id="a50d4-106">時刻 (\* **時** *、* **分** *、* **秒** \*)</span><span class="sxs-lookup"><span data-stu-id="a50d4-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a50d4-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a50d4-107">Parameters</span></span>

|<span data-ttu-id="a50d4-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="a50d4-108">**Name**</span></span>|<span data-ttu-id="a50d4-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="a50d4-109">**Required/Optional**</span></span>|<span data-ttu-id="a50d4-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="a50d4-110">**Data Type**</span></span>|<span data-ttu-id="a50d4-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a50d4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a50d4-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="a50d4-112">_hour_</span></span> <br/> |<span data-ttu-id="a50d4-113">必須</span><span class="sxs-lookup"><span data-stu-id="a50d4-113">Required</span></span>  <br/> |<span data-ttu-id="a50d4-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="a50d4-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a50d4-115">時間のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="a50d4-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="a50d4-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="a50d4-116">_minute_</span></span> <br/> |<span data-ttu-id="a50d4-117">必須</span><span class="sxs-lookup"><span data-stu-id="a50d4-117">Required</span></span>  <br/> |<span data-ttu-id="a50d4-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="a50d4-118">**Numeric**</span></span> <br/> |<span data-ttu-id="a50d4-119">分のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="a50d4-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="a50d4-120">_second_</span><span class="sxs-lookup"><span data-stu-id="a50d4-120">_second_</span></span> <br/> |<span data-ttu-id="a50d4-121">必須</span><span class="sxs-lookup"><span data-stu-id="a50d4-121">Required</span></span>  <br/> |<span data-ttu-id="a50d4-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="a50d4-122">**Numeric**</span></span> <br/> |<span data-ttu-id="a50d4-123">秒のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="a50d4-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a50d4-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="a50d4-124">Return value</span></span>

<span data-ttu-id="a50d4-125">数値</span><span class="sxs-lookup"><span data-stu-id="a50d4-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="a50d4-126">例 1</span><span class="sxs-lookup"><span data-stu-id="a50d4-126">Example 1</span></span>

<span data-ttu-id="a50d4-127">時間 (15、30、30)</span><span class="sxs-lookup"><span data-stu-id="a50d4-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="a50d4-128">15:30:30 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="a50d4-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a50d4-129">例 2</span><span class="sxs-lookup"><span data-stu-id="a50d4-129">Example 2</span></span>

<span data-ttu-id="a50d4-130">FORMAT (TIME (15, 30, 30), "HH: mm")</span><span class="sxs-lookup"><span data-stu-id="a50d4-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="a50d4-131">15:30 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="a50d4-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a50d4-132">例 3</span><span class="sxs-lookup"><span data-stu-id="a50d4-132">Example 3</span></span>

<span data-ttu-id="a50d4-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="a50d4-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="a50d4-134">23:30:30 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="a50d4-134">Returns the value representing 23:30:30.</span></span>
  

