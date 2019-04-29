---
title: BOUNDINGBOXRECT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: 図形の境界ボックスの、指定した端の座標を返します。
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418072"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="afa7d-103">BOUNDINGBOXRECT 関数</span><span class="sxs-lookup"><span data-stu-id="afa7d-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="afa7d-104">図形の境界ボックスの、指定した端の座標を返します。</span><span class="sxs-lookup"><span data-stu-id="afa7d-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="afa7d-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="afa7d-105">Version Information</span></span>

<span data-ttu-id="afa7d-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="afa7d-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="afa7d-107">構文</span><span class="sxs-lookup"><span data-stu-id="afa7d-107">Syntax</span></span>

<span data-ttu-id="afa7d-108">BOUNDINGBOXRECT (\* \* *Index* \* \*)</span><span class="sxs-lookup"><span data-stu-id="afa7d-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="afa7d-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="afa7d-109">Parameters</span></span>

|<span data-ttu-id="afa7d-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="afa7d-110">**Name**</span></span>|<span data-ttu-id="afa7d-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="afa7d-111">**Required/Optional**</span></span>|<span data-ttu-id="afa7d-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="afa7d-112">**Data Type**</span></span>|<span data-ttu-id="afa7d-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="afa7d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="afa7d-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="afa7d-114">_Index_</span></span> <br/> |<span data-ttu-id="afa7d-115">必須</span><span class="sxs-lookup"><span data-stu-id="afa7d-115">Required</span></span>  <br/> |<span data-ttu-id="afa7d-116">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="afa7d-116">**Integer**</span></span> <br/> |<span data-ttu-id="afa7d-117">座標を取得する図形の境界ボックスの端。</span><span class="sxs-lookup"><span data-stu-id="afa7d-117">The edge of the shape's bounding box for which to get the coordinate.</span></span> <span data-ttu-id="afa7d-118">使用可能な値については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="afa7d-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="afa7d-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="afa7d-119">Return value</span></span>

 <span data-ttu-id="afa7d-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="afa7d-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afa7d-121">注釈</span><span class="sxs-lookup"><span data-stu-id="afa7d-121">Remarks</span></span>

 <span data-ttu-id="afa7d-122">*Index*には、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="afa7d-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="afa7d-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="afa7d-123">**Item**</span></span>|<span data-ttu-id="afa7d-124">**値**</span><span class="sxs-lookup"><span data-stu-id="afa7d-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="afa7d-125">左端</span><span class="sxs-lookup"><span data-stu-id="afa7d-125">Left edge</span></span>  <br/> |<span data-ttu-id="afa7d-126">.0</span><span class="sxs-lookup"><span data-stu-id="afa7d-126">0</span></span>  <br/> |
|<span data-ttu-id="afa7d-127">右端</span><span class="sxs-lookup"><span data-stu-id="afa7d-127">Right edge</span></span>  <br/> |<span data-ttu-id="afa7d-128">1 </span><span class="sxs-lookup"><span data-stu-id="afa7d-128">1</span></span>  <br/> |
|<span data-ttu-id="afa7d-129">上端</span><span class="sxs-lookup"><span data-stu-id="afa7d-129">Top edge</span></span>  <br/> |<span data-ttu-id="afa7d-130">2 </span><span class="sxs-lookup"><span data-stu-id="afa7d-130">2</span></span>  <br/> |
|<span data-ttu-id="afa7d-131">下端</span><span class="sxs-lookup"><span data-stu-id="afa7d-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="afa7d-132">3 </span><span class="sxs-lookup"><span data-stu-id="afa7d-132">3</span></span>  <br/> |
   
<span data-ttu-id="afa7d-133">図形に親がある場合、戻り値はその親の座標系になります。</span><span class="sxs-lookup"><span data-stu-id="afa7d-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

