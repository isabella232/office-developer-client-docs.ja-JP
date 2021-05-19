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
description: 時間、分、および秒で表される時間を返します。
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414474"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="ab8a5-103">TIME 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="ab8a5-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="ab8a5-104">時間、分、および  _秒で表_ される  _時間を_ 返  _します_。</span><span class="sxs-lookup"><span data-stu-id="ab8a5-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ab8a5-105">構文</span><span class="sxs-lookup"><span data-stu-id="ab8a5-105">Syntax</span></span>

<span data-ttu-id="ab8a5-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ab8a5-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ab8a5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab8a5-107">Parameters</span></span>

|<span data-ttu-id="ab8a5-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="ab8a5-108">**Name**</span></span>|<span data-ttu-id="ab8a5-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ab8a5-109">**Required/Optional**</span></span>|<span data-ttu-id="ab8a5-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ab8a5-110">**Data Type**</span></span>|<span data-ttu-id="ab8a5-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="ab8a5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ab8a5-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="ab8a5-112">_hour_</span></span> <br/> |<span data-ttu-id="ab8a5-113">必須</span><span class="sxs-lookup"><span data-stu-id="ab8a5-113">Required</span></span>  <br/> |<span data-ttu-id="ab8a5-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="ab8a5-114">**Numeric**</span></span> <br/> |<span data-ttu-id="ab8a5-115">時間のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="ab8a5-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="ab8a5-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="ab8a5-116">_minute_</span></span> <br/> |<span data-ttu-id="ab8a5-117">必須</span><span class="sxs-lookup"><span data-stu-id="ab8a5-117">Required</span></span>  <br/> |<span data-ttu-id="ab8a5-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="ab8a5-118">**Numeric**</span></span> <br/> |<span data-ttu-id="ab8a5-119">分のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="ab8a5-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="ab8a5-120">_second_</span><span class="sxs-lookup"><span data-stu-id="ab8a5-120">_second_</span></span> <br/> |<span data-ttu-id="ab8a5-121">必須</span><span class="sxs-lookup"><span data-stu-id="ab8a5-121">Required</span></span>  <br/> |<span data-ttu-id="ab8a5-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="ab8a5-122">**Numeric**</span></span> <br/> |<span data-ttu-id="ab8a5-123">秒のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="ab8a5-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ab8a5-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="ab8a5-124">Return value</span></span>

<span data-ttu-id="ab8a5-125">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="ab8a5-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ab8a5-126">例 1</span><span class="sxs-lookup"><span data-stu-id="ab8a5-126">Example 1</span></span>

<span data-ttu-id="ab8a5-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="ab8a5-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="ab8a5-128">15:30:30 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ab8a5-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ab8a5-129">例 2</span><span class="sxs-lookup"><span data-stu-id="ab8a5-129">Example 2</span></span>

<span data-ttu-id="ab8a5-130">FORMAT(TIME(15,30,30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="ab8a5-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="ab8a5-131">15:30 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ab8a5-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ab8a5-132">例 3</span><span class="sxs-lookup"><span data-stu-id="ab8a5-132">Example 3</span></span>

<span data-ttu-id="ab8a5-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="ab8a5-134">23:30:30 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ab8a5-134">Returns the value representing 23:30:30.</span></span>
  

