---
title: BOUNDINGBOXDIST 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: 図形の境界ボックスの、指定した部分の測定値を返します。
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804933"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="44725-103">BOUNDINGBOXDIST 関数</span><span class="sxs-lookup"><span data-stu-id="44725-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="44725-104">図形の境界ボックスの、指定した部分の測定値を返します。</span><span class="sxs-lookup"><span data-stu-id="44725-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="44725-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="44725-105">Version Information</span></span>

<span data-ttu-id="44725-106">Visio 2010 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="44725-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="44725-107">構文</span><span class="sxs-lookup"><span data-stu-id="44725-107">Syntax</span></span>

<span data-ttu-id="44725-108">BOUNDINGBOXDIST (* **インデックス** *)</span><span class="sxs-lookup"><span data-stu-id="44725-108">BOUNDINGBOXDIST(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="44725-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="44725-109">Parameters</span></span>

|<span data-ttu-id="44725-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="44725-110">**Name**</span></span>|<span data-ttu-id="44725-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="44725-111">**Required/Optional**</span></span>|<span data-ttu-id="44725-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="44725-112">**Data Type**</span></span>|<span data-ttu-id="44725-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="44725-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="44725-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="44725-114">_Index_</span></span> <br/> |<span data-ttu-id="44725-115">必須</span><span class="sxs-lookup"><span data-stu-id="44725-115">Required</span></span>  <br/> |<span data-ttu-id="44725-116">**番号**</span><span class="sxs-lookup"><span data-stu-id="44725-116">**Number**</span></span> <br/> |<span data-ttu-id="44725-117">図形の一部に外接するボックスを測定し、返します。</span><span class="sxs-lookup"><span data-stu-id="44725-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="44725-118">使用可能な値については備考を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44725-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="44725-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="44725-119">Return value</span></span>

 <span data-ttu-id="44725-120">**番号**</span><span class="sxs-lookup"><span data-stu-id="44725-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44725-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="44725-121">Remarks</span></span>

 <span data-ttu-id="44725-122">*インデックス*には、次の値のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="44725-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="44725-123">**アイテム**</span><span class="sxs-lookup"><span data-stu-id="44725-123">**Item**</span></span>|<span data-ttu-id="44725-124">**値**</span><span class="sxs-lookup"><span data-stu-id="44725-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="44725-125">幅</span><span class="sxs-lookup"><span data-stu-id="44725-125">Width</span></span>  <br/> |<span data-ttu-id="44725-126">0</span><span class="sxs-lookup"><span data-stu-id="44725-126">0</span></span>  <br/> |
|<span data-ttu-id="44725-127">高さ</span><span class="sxs-lookup"><span data-stu-id="44725-127">Height</span></span>  <br/> |<span data-ttu-id="44725-128">1</span><span class="sxs-lookup"><span data-stu-id="44725-128">1</span></span>  <br/> |
|<span data-ttu-id="44725-129">左端から図形のピンまでの距離</span><span class="sxs-lookup"><span data-stu-id="44725-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="44725-130">2</span><span class="sxs-lookup"><span data-stu-id="44725-130">2</span></span>  <br/> |
|<span data-ttu-id="44725-131">図形のピンから右端までの距離</span><span class="sxs-lookup"><span data-stu-id="44725-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="44725-132">3</span><span class="sxs-lookup"><span data-stu-id="44725-132">3</span></span>  <br/> |
|<span data-ttu-id="44725-133">図形のピンから上端までの距離</span><span class="sxs-lookup"><span data-stu-id="44725-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="44725-134">4</span><span class="sxs-lookup"><span data-stu-id="44725-134">4</span></span>  <br/> |
|<span data-ttu-id="44725-135">下端から図形のピンまでの距離</span><span class="sxs-lookup"><span data-stu-id="44725-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="44725-136">5</span><span class="sxs-lookup"><span data-stu-id="44725-136">5</span></span>  <br/> |
|<span data-ttu-id="44725-137">境界ボックスの中心から PinX までの距離</span><span class="sxs-lookup"><span data-stu-id="44725-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="44725-138">6</span><span class="sxs-lookup"><span data-stu-id="44725-138">6</span></span>  <br/> |
|<span data-ttu-id="44725-139">境界ボックスの中心から PinY までの距離</span><span class="sxs-lookup"><span data-stu-id="44725-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="44725-140">7</span><span class="sxs-lookup"><span data-stu-id="44725-140">7</span></span>  <br/> |
   

