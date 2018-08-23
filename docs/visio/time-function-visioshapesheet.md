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
description: 1 時間で表される時刻が返されます、1 分と 1 秒です。
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806667"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="0e8a9-103">TIME 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="0e8a9-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="0e8a9-104">_時間__分_、および_2 つ目_で表される時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="0e8a9-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0e8a9-105">構文</span><span class="sxs-lookup"><span data-stu-id="0e8a9-105">Syntax</span></span>

<span data-ttu-id="0e8a9-106">時間 (* **時間** *、* **分** *、* * *2* * *)</span><span class="sxs-lookup"><span data-stu-id="0e8a9-106">TIME(** *hour* **, ** *minute* **, ** *second* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0e8a9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e8a9-107">Parameters</span></span>

|<span data-ttu-id="0e8a9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="0e8a9-108">**Name**</span></span>|<span data-ttu-id="0e8a9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0e8a9-109">**Required/Optional**</span></span>|<span data-ttu-id="0e8a9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0e8a9-110">**Data Type**</span></span>|<span data-ttu-id="0e8a9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0e8a9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0e8a9-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="0e8a9-112">_hour_</span></span> <br/> |<span data-ttu-id="0e8a9-113">必須</span><span class="sxs-lookup"><span data-stu-id="0e8a9-113">Required</span></span>  <br/> |<span data-ttu-id="0e8a9-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="0e8a9-114">**Numeric**</span></span> <br/> |<span data-ttu-id="0e8a9-115">時間のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="0e8a9-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="0e8a9-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="0e8a9-116">_minute_</span></span> <br/> |<span data-ttu-id="0e8a9-117">必須</span><span class="sxs-lookup"><span data-stu-id="0e8a9-117">Required</span></span>  <br/> |<span data-ttu-id="0e8a9-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="0e8a9-118">**Numeric**</span></span> <br/> |<span data-ttu-id="0e8a9-119">分のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="0e8a9-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="0e8a9-120">_second_</span><span class="sxs-lookup"><span data-stu-id="0e8a9-120">_second_</span></span> <br/> |<span data-ttu-id="0e8a9-121">必須</span><span class="sxs-lookup"><span data-stu-id="0e8a9-121">Required</span></span>  <br/> |<span data-ttu-id="0e8a9-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="0e8a9-122">**Numeric**</span></span> <br/> |<span data-ttu-id="0e8a9-123">秒のコンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="0e8a9-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0e8a9-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e8a9-124">Return value</span></span>

<span data-ttu-id="0e8a9-125">数値</span><span class="sxs-lookup"><span data-stu-id="0e8a9-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="0e8a9-126">例 1</span><span class="sxs-lookup"><span data-stu-id="0e8a9-126">Example 1</span></span>

<span data-ttu-id="0e8a9-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="0e8a9-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="0e8a9-128">15:30:30 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="0e8a9-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0e8a9-129">例 2</span><span class="sxs-lookup"><span data-stu-id="0e8a9-129">Example 2</span></span>

<span data-ttu-id="0e8a9-130">FORMAT(TIME(15,30,30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="0e8a9-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="0e8a9-131">15:30 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="0e8a9-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0e8a9-132">例 3</span><span class="sxs-lookup"><span data-stu-id="0e8a9-132">Example 3</span></span>

<span data-ttu-id="0e8a9-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="0e8a9-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="0e8a9-134">23:30:30 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="0e8a9-134">Returns the value representing 23:30:30.</span></span>
  

