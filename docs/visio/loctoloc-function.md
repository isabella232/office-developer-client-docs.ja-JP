---
title: LOCTOLOC 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: 変換後の座標系のローカル座標に変換された点を返します。
ms.openlocfilehash: f08feb6137c3022027d19b45f06285fb8b6441a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358038"
---
# <a name="loctoloc-function"></a><span data-ttu-id="0fd3e-103">LOCTOLOC 関数</span><span class="sxs-lookup"><span data-stu-id="0fd3e-103">LOCTOLOC Function</span></span>

<span data-ttu-id="0fd3e-104">変換後の座標系のローカル座標に変換された点を返します。</span><span class="sxs-lookup"><span data-stu-id="0fd3e-104">Returns a transformed point in local coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0fd3e-105">構文</span><span class="sxs-lookup"><span data-stu-id="0fd3e-105">Syntax</span></span>

<span data-ttu-id="0fd3e-106">loctoloc (\* \* *srcpoint* \* \*, \* \* *srcref* \* \*, \* \* *dstref* \* \*)</span><span class="sxs-lookup"><span data-stu-id="0fd3e-106">LOCTOLOC(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0fd3e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0fd3e-107">Parameters</span></span>

|<span data-ttu-id="0fd3e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="0fd3e-108">**Name**</span></span>|<span data-ttu-id="0fd3e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0fd3e-109">**Required/Optional**</span></span>|<span data-ttu-id="0fd3e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0fd3e-110">**Data Type**</span></span>|<span data-ttu-id="0fd3e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0fd3e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0fd3e-112">_srcpoint_</span><span class="sxs-lookup"><span data-stu-id="0fd3e-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="0fd3e-113">必須</span><span class="sxs-lookup"><span data-stu-id="0fd3e-113">Required</span></span>  <br/> |<span data-ttu-id="0fd3e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="0fd3e-114">**String**</span></span> <br/> | <span data-ttu-id="0fd3e-115">変換元の座標系でのローカル座標の点を指定します。</span><span class="sxs-lookup"><span data-stu-id="0fd3e-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="0fd3e-116">_srcref_</span><span class="sxs-lookup"><span data-stu-id="0fd3e-116">_srcRef_</span></span> <br/> |<span data-ttu-id="0fd3e-117">必須</span><span class="sxs-lookup"><span data-stu-id="0fd3e-117">Required</span></span>  <br/> |<span data-ttu-id="0fd3e-118">**String**</span><span class="sxs-lookup"><span data-stu-id="0fd3e-118">**String**</span></span> <br/> | <span data-ttu-id="0fd3e-119">変換元オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="0fd3e-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="0fd3e-120">_dstref_</span><span class="sxs-lookup"><span data-stu-id="0fd3e-120">_dstRef_</span></span> <br/> |<span data-ttu-id="0fd3e-121">必須</span><span class="sxs-lookup"><span data-stu-id="0fd3e-121">Required</span></span>  <br/> |<span data-ttu-id="0fd3e-122">**String**</span><span class="sxs-lookup"><span data-stu-id="0fd3e-122">**String**</span></span> <br/> | <span data-ttu-id="0fd3e-123">変換先オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="0fd3e-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0fd3e-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="0fd3e-124">Return value</span></span>

<span data-ttu-id="0fd3e-125">文字列</span><span class="sxs-lookup"><span data-stu-id="0fd3e-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0fd3e-126">注釈</span><span class="sxs-lookup"><span data-stu-id="0fd3e-126">Remarks</span></span>

<span data-ttu-id="0fd3e-p101">LOCTOLOC 関数は、変換元図形のローカル座標の点を、変換先図形のローカル座標に変換します。この関数を使用すると、別の座標空間の点に基づいて図形を作成できます。またローカルな点をページ座標に変換したり、ページ座標をローカルな点に変換することもできます。</span><span class="sxs-lookup"><span data-stu-id="0fd3e-p101">The LOCTOLOC function converts a point from local coordinates in a source shape to local coordinates in a destination shape. You can use this function to construct a shape, for example, in terms of a point from another coordinate space. You can also use this function to transform a local point to page coordinates, or vice versa.</span></span>
  
<span data-ttu-id="0fd3e-p102">変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。</span><span class="sxs-lookup"><span data-stu-id="0fd3e-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="0fd3e-132">変換元図形と変換先図形の座標は、同じページ上になければなりません。</span><span class="sxs-lookup"><span data-stu-id="0fd3e-132">The source and destination coordinates must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="0fd3e-133">例</span><span class="sxs-lookup"><span data-stu-id="0fd3e-133">Example</span></span>

<span data-ttu-id="0fd3e-134">次の数式は、数式に関連付けられている図形のローカル Pin をページ上の点に変換します。</span><span class="sxs-lookup"><span data-stu-id="0fd3e-134">The following formula converts the local pin of the shape associated with the formula to a point on the page.</span></span>
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


