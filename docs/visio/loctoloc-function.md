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
description: 変換先の座標系でのローカル座標に変換した点を返します。
ms.openlocfilehash: 444200801ebd984fb735b95de6d58d35e5160d1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805804"
---
# <a name="loctoloc-function"></a><span data-ttu-id="9a712-103">LOCTOLOC 関数</span><span class="sxs-lookup"><span data-stu-id="9a712-103">LOCTOLOC Function</span></span>

<span data-ttu-id="9a712-104">変換先の座標系でのローカル座標に変換した点を返します。</span><span class="sxs-lookup"><span data-stu-id="9a712-104">Returns a transformed point in local coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9a712-105">構文</span><span class="sxs-lookup"><span data-stu-id="9a712-105">Syntax</span></span>

<span data-ttu-id="9a712-106">LOCTOLOC (* * *srcPoint* * *、* * *srcRef* * *、* * *dstRef* * *)</span><span class="sxs-lookup"><span data-stu-id="9a712-106">LOCTOLOC(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9a712-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="9a712-107">Parameters</span></span>

|<span data-ttu-id="9a712-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="9a712-108">**Name**</span></span>|<span data-ttu-id="9a712-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="9a712-109">**Required/Optional**</span></span>|<span data-ttu-id="9a712-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="9a712-110">**Data Type**</span></span>|<span data-ttu-id="9a712-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="9a712-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9a712-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="9a712-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="9a712-113">必須</span><span class="sxs-lookup"><span data-stu-id="9a712-113">Required</span></span>  <br/> |<span data-ttu-id="9a712-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="9a712-114">**String**</span></span> <br/> | <span data-ttu-id="9a712-115">変換元の座標系でのローカル座標の点を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a712-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="9a712-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="9a712-116">_srcRef_</span></span> <br/> |<span data-ttu-id="9a712-117">必須</span><span class="sxs-lookup"><span data-stu-id="9a712-117">Required</span></span>  <br/> |<span data-ttu-id="9a712-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="9a712-118">**String**</span></span> <br/> | <span data-ttu-id="9a712-119">変換元オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a712-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="9a712-120">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="9a712-120">_dstRef_</span></span> <br/> |<span data-ttu-id="9a712-121">必須</span><span class="sxs-lookup"><span data-stu-id="9a712-121">Required</span></span>  <br/> |<span data-ttu-id="9a712-122">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="9a712-122">**String**</span></span> <br/> | <span data-ttu-id="9a712-123">変換先オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a712-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9a712-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9a712-124">Return value</span></span>

<span data-ttu-id="9a712-125">文字列</span><span class="sxs-lookup"><span data-stu-id="9a712-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a712-126">注釈</span><span class="sxs-lookup"><span data-stu-id="9a712-126">Remarks</span></span>

<span data-ttu-id="9a712-p101">LOCTOLOC 関数は、変換元図形のローカル座標の点を、変換先図形のローカル座標に変換します。この関数を使用すると、別の座標空間の点に基づいて図形を作成できます。またローカルな点をページ座標に変換したり、ページ座標をローカルな点に変換することもできます。</span><span class="sxs-lookup"><span data-stu-id="9a712-p101">The LOCTOLOC function converts a point from local coordinates in a source shape to local coordinates in a destination shape. You can use this function to construct a shape, for example, in terms of a point from another coordinate space. You can also use this function to transform a local point to page coordinates, or vice versa.</span></span>
  
<span data-ttu-id="9a712-p102">変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。</span><span class="sxs-lookup"><span data-stu-id="9a712-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="9a712-132">変換元図形と変換先図形の座標は、同じページ上になければなりません。</span><span class="sxs-lookup"><span data-stu-id="9a712-132">The source and destination coordinates must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="9a712-133">例</span><span class="sxs-lookup"><span data-stu-id="9a712-133">Example</span></span>

<span data-ttu-id="9a712-134">次の数式は、数式に関連付けられている図形のローカル Pin をページ上の点に変換します。</span><span class="sxs-lookup"><span data-stu-id="9a712-134">The following formula converts the local pin of the shape associated with the formula to a point on the page.</span></span>
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


