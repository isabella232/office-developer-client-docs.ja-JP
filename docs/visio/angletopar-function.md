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
description: 変換先図形の親座標系に変換された角度を返します。 角度を接続元の図形のローカル座標から変換先図形の親座標に変換します。
ms.openlocfilehash: 3a739c55d568dc548f8175b56f22e6ec4c28e4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804785"
---
# <a name="angletopar-function"></a><span data-ttu-id="d5257-104">ANGLETOPAR 関数</span><span class="sxs-lookup"><span data-stu-id="d5257-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="d5257-105">変換先図形の親座標系に変換された角度を返します。</span><span class="sxs-lookup"><span data-stu-id="d5257-105">Returns a transformed angle in the destination shape's parent coordinate system.</span></span> <span data-ttu-id="d5257-106">角度を接続元の図形のローカル座標から変換先図形の親座標に変換します。</span><span class="sxs-lookup"><span data-stu-id="d5257-106">Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d5257-107">構文</span><span class="sxs-lookup"><span data-stu-id="d5257-107">Syntax</span></span>

<span data-ttu-id="d5257-108">ANGLETOPAR (* * *srcAngle* * *、* * *srcRef* * *、* * *dstRef* * *)</span><span class="sxs-lookup"><span data-stu-id="d5257-108">ANGLETOPAR(** *srcAngle* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d5257-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="d5257-109">Parameters</span></span>

|<span data-ttu-id="d5257-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="d5257-110">**Name**</span></span>|<span data-ttu-id="d5257-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d5257-111">**Required/Optional**</span></span>|<span data-ttu-id="d5257-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d5257-112">**Data Type**</span></span>|<span data-ttu-id="d5257-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5257-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d5257-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="d5257-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="d5257-115">必須</span><span class="sxs-lookup"><span data-stu-id="d5257-115">Required</span></span>  <br/> |<span data-ttu-id="d5257-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="d5257-116">**Numeric**</span></span> <br/> |<span data-ttu-id="d5257-117">変換元座標系での角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5257-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="d5257-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="d5257-118">_srcRef_</span></span> <br/> |<span data-ttu-id="d5257-119">必須</span><span class="sxs-lookup"><span data-stu-id="d5257-119">Required</span></span>  <br/> |<span data-ttu-id="d5257-120">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="d5257-120">**String**</span></span> <br/> | <span data-ttu-id="d5257-121">図形、グループ、ページなどの変換元オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5257-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="d5257-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="d5257-122">_dstRef_</span></span> <br/> |<span data-ttu-id="d5257-123">必須</span><span class="sxs-lookup"><span data-stu-id="d5257-123">Required</span></span>  <br/> |<span data-ttu-id="d5257-124">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="d5257-124">**String**</span></span> <br/> |<span data-ttu-id="d5257-125">図形、グループ、ページなどの変換先オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5257-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5257-126">注釈</span><span class="sxs-lookup"><span data-stu-id="d5257-126">Remarks</span></span>

<span data-ttu-id="d5257-p103">変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。</span><span class="sxs-lookup"><span data-stu-id="d5257-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="d5257-129">変換元図形と変換先図形の座標は、同じページ上になければなりません。</span><span class="sxs-lookup"><span data-stu-id="d5257-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="d5257-130">変換先がページで、親図形がない場合、ページのローカル座標で結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5257-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

