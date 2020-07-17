---
title: ANGLETOLOC 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: 変換先図形のローカル座標系に変換された角度を返します。 つまり、変換元図形のローカル座標から変換先図形のローカル座標に、角度が変換されます。
ms.openlocfilehash: e971613d4fc33cd991e7e9aeba49ac47871ebe8f
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160266"
---
# <a name="angletoloc-function"></a><span data-ttu-id="90558-104">ANGLETOLOC 関数</span><span class="sxs-lookup"><span data-stu-id="90558-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="90558-105">変換先図形のローカル座標系に変換された角度を返します。</span><span class="sxs-lookup"><span data-stu-id="90558-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="90558-106">つまり、変換元図形のローカル座標から変換先図形のローカル座標に、角度が変換されます。</span><span class="sxs-lookup"><span data-stu-id="90558-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="90558-107">構文</span><span class="sxs-lookup"><span data-stu-id="90558-107">Syntax</span></span>

<span data-ttu-id="90558-108">ANGLETOLOC (***Srcangle***、 ***srcref***、 ***dstref*** )</span><span class="sxs-lookup"><span data-stu-id="90558-108">ANGLETOLOC(***srcAngle***, ***srcRef***, ***dstRef*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="90558-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="90558-109">Parameters</span></span>

|<span data-ttu-id="90558-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="90558-110">**Name**</span></span>|<span data-ttu-id="90558-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="90558-111">**Required/Optional**</span></span>|<span data-ttu-id="90558-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="90558-112">**Data Type**</span></span>|<span data-ttu-id="90558-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="90558-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="90558-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="90558-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="90558-115">必須</span><span class="sxs-lookup"><span data-stu-id="90558-115">Required</span></span>  <br/> |<span data-ttu-id="90558-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="90558-116">**Numeric**</span></span> <br/> |<span data-ttu-id="90558-117">変換元座標系での角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="90558-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="90558-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="90558-118">_srcRef_</span></span> <br/> |<span data-ttu-id="90558-119">必須</span><span class="sxs-lookup"><span data-stu-id="90558-119">Required</span></span>  <br/> |<span data-ttu-id="90558-120">**String**</span><span class="sxs-lookup"><span data-stu-id="90558-120">**String**</span></span> <br/> | <span data-ttu-id="90558-121">図形、グループ、ページなどの変換元オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="90558-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="90558-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="90558-122">_dstRef_</span></span> <br/> |<span data-ttu-id="90558-123">必須</span><span class="sxs-lookup"><span data-stu-id="90558-123">Required</span></span>  <br/> |<span data-ttu-id="90558-124">**String**</span><span class="sxs-lookup"><span data-stu-id="90558-124">**String**</span></span> <br/> |<span data-ttu-id="90558-125">図形、グループ、ページなどの変換先オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="90558-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90558-126">備考</span><span class="sxs-lookup"><span data-stu-id="90558-126">Remarks</span></span>

<span data-ttu-id="90558-127">ANGLETOLOC 関数を使用すると、別の座標空間の角度に基づいて、図形内にあるローカルの角度のセルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="90558-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="90558-p103">変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。</span><span class="sxs-lookup"><span data-stu-id="90558-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="90558-130">変換元図形と変換先図形の座標は、同じページ上になければなりません。</span><span class="sxs-lookup"><span data-stu-id="90558-130">The source and destination coordinates must be on the same page.</span></span>
  

