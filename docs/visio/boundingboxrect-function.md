---
title: BOUNDINGBOXRECT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: 図形の境界ボックスの、指定した端の座標を返します。
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804928"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="307ee-103">BOUNDINGBOXRECT 関数</span><span class="sxs-lookup"><span data-stu-id="307ee-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="307ee-104">図形の境界ボックスの、指定した端の座標を返します。</span><span class="sxs-lookup"><span data-stu-id="307ee-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="307ee-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="307ee-105">Version Information</span></span>

<span data-ttu-id="307ee-106">Visio 2010 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="307ee-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="307ee-107">構文</span><span class="sxs-lookup"><span data-stu-id="307ee-107">Syntax</span></span>

<span data-ttu-id="307ee-108">BOUNDINGBOXRECT (* **インデックス** *)</span><span class="sxs-lookup"><span data-stu-id="307ee-108">BOUNDINGBOXRECT(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="307ee-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="307ee-109">Parameters</span></span>

|<span data-ttu-id="307ee-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="307ee-110">**Name**</span></span>|<span data-ttu-id="307ee-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="307ee-111">**Required/Optional**</span></span>|<span data-ttu-id="307ee-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="307ee-112">**Data Type**</span></span>|<span data-ttu-id="307ee-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="307ee-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="307ee-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="307ee-114">_Index_</span></span> <br/> |<span data-ttu-id="307ee-115">必須</span><span class="sxs-lookup"><span data-stu-id="307ee-115">Required</span></span>  <br/> |<span data-ttu-id="307ee-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="307ee-116">**Integer**</span></span> <br/> |<span data-ttu-id="307ee-p101">座標を取得する図形の境界ボックスの端。使用可能な値については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="307ee-p101">The edge of the shape's bounding box for which to get the coordinate. See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="307ee-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="307ee-119">Return value</span></span>

 <span data-ttu-id="307ee-120">**番号**</span><span class="sxs-lookup"><span data-stu-id="307ee-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="307ee-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="307ee-121">Remarks</span></span>

 <span data-ttu-id="307ee-122">*インデックス*には、次の値のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="307ee-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="307ee-123">**アイテム**</span><span class="sxs-lookup"><span data-stu-id="307ee-123">**Item**</span></span>|<span data-ttu-id="307ee-124">**値**</span><span class="sxs-lookup"><span data-stu-id="307ee-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="307ee-125">左端</span><span class="sxs-lookup"><span data-stu-id="307ee-125">Left edge</span></span>  <br/> |<span data-ttu-id="307ee-126">0</span><span class="sxs-lookup"><span data-stu-id="307ee-126">0</span></span>  <br/> |
|<span data-ttu-id="307ee-127">右端</span><span class="sxs-lookup"><span data-stu-id="307ee-127">Right edge</span></span>  <br/> |<span data-ttu-id="307ee-128">1</span><span class="sxs-lookup"><span data-stu-id="307ee-128">1</span></span>  <br/> |
|<span data-ttu-id="307ee-129">上端</span><span class="sxs-lookup"><span data-stu-id="307ee-129">Top edge</span></span>  <br/> |<span data-ttu-id="307ee-130">2</span><span class="sxs-lookup"><span data-stu-id="307ee-130">2</span></span>  <br/> |
|<span data-ttu-id="307ee-131">下端</span><span class="sxs-lookup"><span data-stu-id="307ee-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="307ee-132">3</span><span class="sxs-lookup"><span data-stu-id="307ee-132">3</span></span>  <br/> |
   
<span data-ttu-id="307ee-133">図形に親がある場合、戻り値はその親の座標系では。</span><span class="sxs-lookup"><span data-stu-id="307ee-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  
