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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338053"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="ca175-103">BOUNDINGBOXRECT 関数</span><span class="sxs-lookup"><span data-stu-id="ca175-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="ca175-104">図形の境界ボックスの、指定した端の座標を返します。</span><span class="sxs-lookup"><span data-stu-id="ca175-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="ca175-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="ca175-105">Version Information</span></span>

<span data-ttu-id="ca175-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="ca175-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ca175-107">構文</span><span class="sxs-lookup"><span data-stu-id="ca175-107">Syntax</span></span>

<span data-ttu-id="ca175-108">BOUNDINGBOXRECT (\* \* *Index* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ca175-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ca175-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca175-109">Parameters</span></span>

|<span data-ttu-id="ca175-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="ca175-110">**Name**</span></span>|<span data-ttu-id="ca175-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ca175-111">**Required/Optional**</span></span>|<span data-ttu-id="ca175-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ca175-112">**Data Type**</span></span>|<span data-ttu-id="ca175-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="ca175-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ca175-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="ca175-114">_Index_</span></span> <br/> |<span data-ttu-id="ca175-115">必須</span><span class="sxs-lookup"><span data-stu-id="ca175-115">Required</span></span>  <br/> |<span data-ttu-id="ca175-116">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="ca175-116">**Integer**</span></span> <br/> |<span data-ttu-id="ca175-117">座標を取得する図形の境界ボックスの端。</span><span class="sxs-lookup"><span data-stu-id="ca175-117">The edge of the shape's bounding box for which to get the coordinate.</span></span> <span data-ttu-id="ca175-118">使用可能な値については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca175-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ca175-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="ca175-119">Return value</span></span>

 <span data-ttu-id="ca175-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="ca175-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca175-121">解説</span><span class="sxs-lookup"><span data-stu-id="ca175-121">Remarks</span></span>

 <span data-ttu-id="ca175-122">*Index*には、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ca175-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="ca175-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="ca175-123">**Item**</span></span>|<span data-ttu-id="ca175-124">**値**</span><span class="sxs-lookup"><span data-stu-id="ca175-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca175-125">左端</span><span class="sxs-lookup"><span data-stu-id="ca175-125">Left edge</span></span>  <br/> |<span data-ttu-id="ca175-126">.0</span><span class="sxs-lookup"><span data-stu-id="ca175-126">0</span></span>  <br/> |
|<span data-ttu-id="ca175-127">右端</span><span class="sxs-lookup"><span data-stu-id="ca175-127">Right edge</span></span>  <br/> |<span data-ttu-id="ca175-128">1-d</span><span class="sxs-lookup"><span data-stu-id="ca175-128">1</span></span>  <br/> |
|<span data-ttu-id="ca175-129">上端</span><span class="sxs-lookup"><span data-stu-id="ca175-129">Top edge</span></span>  <br/> |<span data-ttu-id="ca175-130">pbm-2</span><span class="sxs-lookup"><span data-stu-id="ca175-130">2</span></span>  <br/> |
|<span data-ttu-id="ca175-131">下端</span><span class="sxs-lookup"><span data-stu-id="ca175-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="ca175-132">1/3</span><span class="sxs-lookup"><span data-stu-id="ca175-132">3</span></span>  <br/> |
   
<span data-ttu-id="ca175-133">図形に親がある場合、戻り値はその親の座標系になります。</span><span class="sxs-lookup"><span data-stu-id="ca175-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

