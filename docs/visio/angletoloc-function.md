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
description: 変換先図形のローカル座標系に変換された角度を返します。 角度を接続元の図形のローカル座標から変換先図形のローカル座標に変換します。
ms.openlocfilehash: 09ab0a4a55446dd74729f1da0bcf022d8376909b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804777"
---
# <a name="angletoloc-function"></a><span data-ttu-id="1e9e1-104">ANGLETOLOC 関数</span><span class="sxs-lookup"><span data-stu-id="1e9e1-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="1e9e1-105">変換先図形のローカル座標系に変換された角度を返します。</span><span class="sxs-lookup"><span data-stu-id="1e9e1-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="1e9e1-106">角度を接続元の図形のローカル座標から変換先図形のローカル座標に変換します。</span><span class="sxs-lookup"><span data-stu-id="1e9e1-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1e9e1-107">構文</span><span class="sxs-lookup"><span data-stu-id="1e9e1-107">Syntax</span></span>

<span data-ttu-id="1e9e1-108">ANGLETOLOC (* * *srcAngle* * *、* * *srcRef* * *、* * *dstRef* * *)</span><span class="sxs-lookup"><span data-stu-id="1e9e1-108">ANGLETOLOC(** *srcAngle* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1e9e1-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="1e9e1-109">Parameters</span></span>

|<span data-ttu-id="1e9e1-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="1e9e1-110">**Name**</span></span>|<span data-ttu-id="1e9e1-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="1e9e1-111">**Required/Optional**</span></span>|<span data-ttu-id="1e9e1-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="1e9e1-112">**Data Type**</span></span>|<span data-ttu-id="1e9e1-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e9e1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1e9e1-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="1e9e1-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="1e9e1-115">必須</span><span class="sxs-lookup"><span data-stu-id="1e9e1-115">Required</span></span>  <br/> |<span data-ttu-id="1e9e1-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="1e9e1-116">**Numeric**</span></span> <br/> |<span data-ttu-id="1e9e1-117">変換元座標系での角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="1e9e1-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="1e9e1-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="1e9e1-118">_srcRef_</span></span> <br/> |<span data-ttu-id="1e9e1-119">必須</span><span class="sxs-lookup"><span data-stu-id="1e9e1-119">Required</span></span>  <br/> |<span data-ttu-id="1e9e1-120">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="1e9e1-120">**String**</span></span> <br/> | <span data-ttu-id="1e9e1-121">図形、グループ、ページなどの変換元オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="1e9e1-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="1e9e1-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="1e9e1-122">_dstRef_</span></span> <br/> |<span data-ttu-id="1e9e1-123">必須</span><span class="sxs-lookup"><span data-stu-id="1e9e1-123">Required</span></span>  <br/> |<span data-ttu-id="1e9e1-124">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="1e9e1-124">**String**</span></span> <br/> |<span data-ttu-id="1e9e1-125">図形、グループ、ページなどの変換先オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="1e9e1-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e9e1-126">注釈</span><span class="sxs-lookup"><span data-stu-id="1e9e1-126">Remarks</span></span>

<span data-ttu-id="1e9e1-127">ANGLETOLOC 関数を使用すると、別の座標空間の角度に基づいて、図形内にあるローカルの角度のセルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1e9e1-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="1e9e1-p103">変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。</span><span class="sxs-lookup"><span data-stu-id="1e9e1-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="1e9e1-130">変換元図形と変換先図形の座標は、同じページ上になければなりません。</span><span class="sxs-lookup"><span data-stu-id="1e9e1-130">The source and destination coordinates must be on the same page.</span></span>
  

