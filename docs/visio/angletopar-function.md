---
title: ANGLETOPAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: 変換先図形の親座標系に基づいて変換された角度を返します。 つまり、変換元図形のローカル座標から変換先図形の親座標に、角度が変換されます。
ms.openlocfilehash: 0fed51e264bfb21da25d4e91f20f4bc0803e46e8
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160259"
---
# <a name="angletopar-function"></a><span data-ttu-id="3255b-104">ANGLETOPAR 関数</span><span class="sxs-lookup"><span data-stu-id="3255b-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="3255b-105">変換先図形の親座標系に基づいて変換された角度を返します。</span><span class="sxs-lookup"><span data-stu-id="3255b-105">Returns a transformed angle in the destination shape's parent coordinate system.</span></span> <span data-ttu-id="3255b-106">つまり、変換元図形のローカル座標から変換先図形の親座標に、角度が変換されます。</span><span class="sxs-lookup"><span data-stu-id="3255b-106">Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3255b-107">構文</span><span class="sxs-lookup"><span data-stu-id="3255b-107">Syntax</span></span>

<span data-ttu-id="3255b-108">ANGLETOPAR (***Srcangle***、 ***srcref***、 ***dstref*** )</span><span class="sxs-lookup"><span data-stu-id="3255b-108">ANGLETOPAR(***srcAngle***, ***srcRef***, ***dstRef*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3255b-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3255b-109">Parameters</span></span>

|<span data-ttu-id="3255b-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="3255b-110">**Name**</span></span>|<span data-ttu-id="3255b-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3255b-111">**Required/Optional**</span></span>|<span data-ttu-id="3255b-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3255b-112">**Data Type**</span></span>|<span data-ttu-id="3255b-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="3255b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3255b-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="3255b-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="3255b-115">必須</span><span class="sxs-lookup"><span data-stu-id="3255b-115">Required</span></span>  <br/> |<span data-ttu-id="3255b-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="3255b-116">**Numeric**</span></span> <br/> |<span data-ttu-id="3255b-117">変換元座標系での角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="3255b-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="3255b-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="3255b-118">_srcRef_</span></span> <br/> |<span data-ttu-id="3255b-119">必須</span><span class="sxs-lookup"><span data-stu-id="3255b-119">Required</span></span>  <br/> |<span data-ttu-id="3255b-120">**String**</span><span class="sxs-lookup"><span data-stu-id="3255b-120">**String**</span></span> <br/> | <span data-ttu-id="3255b-121">図形、グループ、ページなどの変換元オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="3255b-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="3255b-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="3255b-122">_dstRef_</span></span> <br/> |<span data-ttu-id="3255b-123">必須</span><span class="sxs-lookup"><span data-stu-id="3255b-123">Required</span></span>  <br/> |<span data-ttu-id="3255b-124">**String**</span><span class="sxs-lookup"><span data-stu-id="3255b-124">**String**</span></span> <br/> |<span data-ttu-id="3255b-125">図形、グループ、ページなどの変換先オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="3255b-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3255b-126">備考</span><span class="sxs-lookup"><span data-stu-id="3255b-126">Remarks</span></span>

<span data-ttu-id="3255b-p103">変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。</span><span class="sxs-lookup"><span data-stu-id="3255b-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="3255b-129">変換元図形と変換先図形の座標は、同じページ上になければなりません。</span><span class="sxs-lookup"><span data-stu-id="3255b-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="3255b-130">変換先がページで、親図形がない場合、ページのローカル座標で結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3255b-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

