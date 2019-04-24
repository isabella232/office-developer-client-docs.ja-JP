---
title: BOUNDINGBOXDIST 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: 図形の境界ボックスの、指定した部分の測定値を返します。
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348966"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="b0de0-103">BOUNDINGBOXDIST 関数</span><span class="sxs-lookup"><span data-stu-id="b0de0-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="b0de0-104">図形の境界ボックスの、指定した部分の測定値を返します。</span><span class="sxs-lookup"><span data-stu-id="b0de0-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="b0de0-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="b0de0-105">Version Information</span></span>

<span data-ttu-id="b0de0-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="b0de0-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b0de0-107">構文</span><span class="sxs-lookup"><span data-stu-id="b0de0-107">Syntax</span></span>

<span data-ttu-id="b0de0-108">BOUNDINGBOXDIST (\* \* *Index* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b0de0-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b0de0-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0de0-109">Parameters</span></span>

|<span data-ttu-id="b0de0-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="b0de0-110">**Name**</span></span>|<span data-ttu-id="b0de0-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="b0de0-111">**Required/Optional**</span></span>|<span data-ttu-id="b0de0-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="b0de0-112">**Data Type**</span></span>|<span data-ttu-id="b0de0-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="b0de0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b0de0-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="b0de0-114">_Index_</span></span> <br/> |<span data-ttu-id="b0de0-115">必須</span><span class="sxs-lookup"><span data-stu-id="b0de0-115">Required</span></span>  <br/> |<span data-ttu-id="b0de0-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="b0de0-116">**Number**</span></span> <br/> |<span data-ttu-id="b0de0-117">図形の境界ボックスの、測定して返す部分。</span><span class="sxs-lookup"><span data-stu-id="b0de0-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="b0de0-118">使用可能な値については備考を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0de0-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b0de0-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="b0de0-119">Return value</span></span>

 <span data-ttu-id="b0de0-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="b0de0-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0de0-121">解説</span><span class="sxs-lookup"><span data-stu-id="b0de0-121">Remarks</span></span>

 <span data-ttu-id="b0de0-122">*Index*には、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b0de0-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="b0de0-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="b0de0-123">**Item**</span></span>|<span data-ttu-id="b0de0-124">**値**</span><span class="sxs-lookup"><span data-stu-id="b0de0-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0de0-125">Width</span><span class="sxs-lookup"><span data-stu-id="b0de0-125">Width</span></span>  <br/> |<span data-ttu-id="b0de0-126">.0</span><span class="sxs-lookup"><span data-stu-id="b0de0-126">0</span></span>  <br/> |
|<span data-ttu-id="b0de0-127">Height</span><span class="sxs-lookup"><span data-stu-id="b0de0-127">Height</span></span>  <br/> |<span data-ttu-id="b0de0-128">1-d</span><span class="sxs-lookup"><span data-stu-id="b0de0-128">1</span></span>  <br/> |
|<span data-ttu-id="b0de0-129">左端から図形のピンまでの距離</span><span class="sxs-lookup"><span data-stu-id="b0de0-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="b0de0-130">pbm-2</span><span class="sxs-lookup"><span data-stu-id="b0de0-130">2</span></span>  <br/> |
|<span data-ttu-id="b0de0-131">図形のピンから右端までの距離</span><span class="sxs-lookup"><span data-stu-id="b0de0-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="b0de0-132">1/3</span><span class="sxs-lookup"><span data-stu-id="b0de0-132">3</span></span>  <br/> |
|<span data-ttu-id="b0de0-133">図形のピンから上端までの距離</span><span class="sxs-lookup"><span data-stu-id="b0de0-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="b0de0-134">2/4</span><span class="sxs-lookup"><span data-stu-id="b0de0-134">4</span></span>  <br/> |
|<span data-ttu-id="b0de0-135">下端から図形のピンまでの距離</span><span class="sxs-lookup"><span data-stu-id="b0de0-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="b0de0-136">5</span><span class="sxs-lookup"><span data-stu-id="b0de0-136">5</span></span>  <br/> |
|<span data-ttu-id="b0de0-137">境界ボックスの中心から PinX までの距離</span><span class="sxs-lookup"><span data-stu-id="b0de0-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="b0de0-138">シックス</span><span class="sxs-lookup"><span data-stu-id="b0de0-138">6</span></span>  <br/> |
|<span data-ttu-id="b0de0-139">境界ボックスの中心から PinY までの距離</span><span class="sxs-lookup"><span data-stu-id="b0de0-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="b0de0-140">7</span><span class="sxs-lookup"><span data-stu-id="b0de0-140">7</span></span>  <br/> |
   

