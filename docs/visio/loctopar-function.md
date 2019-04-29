---
title: LOCTOPAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: 変換後の座標系の親座標の点を返します。
ms.openlocfilehash: 65a08837d7d026836ebc8d5e35938ea049d005e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439983"
---
# <a name="loctopar-function"></a><span data-ttu-id="35be9-103">LOCTOPAR 関数</span><span class="sxs-lookup"><span data-stu-id="35be9-103">LOCTOPAR Function</span></span>

<span data-ttu-id="35be9-104">変換後の座標系の親座標の点を返します。</span><span class="sxs-lookup"><span data-stu-id="35be9-104">Returns a transformed point in parent coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="35be9-105">構文</span><span class="sxs-lookup"><span data-stu-id="35be9-105">Syntax</span></span>

<span data-ttu-id="35be9-106">loctopar (\* \* *srcpoint* \* \*, \* \* *srcref* \* \*, \* \* *dstref* \* \*)</span><span class="sxs-lookup"><span data-stu-id="35be9-106">LOCTOPAR(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="35be9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35be9-107">Parameters</span></span>

|<span data-ttu-id="35be9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="35be9-108">**Name**</span></span>|<span data-ttu-id="35be9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="35be9-109">**Required/Optional**</span></span>|<span data-ttu-id="35be9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="35be9-110">**Data Type**</span></span>|<span data-ttu-id="35be9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="35be9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="35be9-112">_srcpoint_</span><span class="sxs-lookup"><span data-stu-id="35be9-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="35be9-113">必須</span><span class="sxs-lookup"><span data-stu-id="35be9-113">Required</span></span>  <br/> |<span data-ttu-id="35be9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="35be9-114">**String**</span></span> <br/> | <span data-ttu-id="35be9-115">変換元の座標系でのローカル座標の点を指定します。</span><span class="sxs-lookup"><span data-stu-id="35be9-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="35be9-116">_srcref_</span><span class="sxs-lookup"><span data-stu-id="35be9-116">_srcRef_</span></span> <br/> |<span data-ttu-id="35be9-117">必須</span><span class="sxs-lookup"><span data-stu-id="35be9-117">Required</span></span>  <br/> |<span data-ttu-id="35be9-118">**String**</span><span class="sxs-lookup"><span data-stu-id="35be9-118">**String**</span></span> <br/> | <span data-ttu-id="35be9-119">変換元オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="35be9-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="35be9-120">_dstref_</span><span class="sxs-lookup"><span data-stu-id="35be9-120">_dstRef_</span></span> <br/> |<span data-ttu-id="35be9-121">必須</span><span class="sxs-lookup"><span data-stu-id="35be9-121">Required</span></span>  <br/> |<span data-ttu-id="35be9-122">**String**</span><span class="sxs-lookup"><span data-stu-id="35be9-122">**String**</span></span> <br/> | <span data-ttu-id="35be9-123">変換先オブジェクトのセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="35be9-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="35be9-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="35be9-124">Return value</span></span>

<span data-ttu-id="35be9-125">文字列</span><span class="sxs-lookup"><span data-stu-id="35be9-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35be9-126">注釈</span><span class="sxs-lookup"><span data-stu-id="35be9-126">Remarks</span></span>

<span data-ttu-id="35be9-p101">変換元図形のローカル座標から変換先図形の親座標に、点が変換されます。LOCTOPAR 関数を使用すると、別の座標系にある別の点に基づいて、図形の [PinX]、[PinY]、[BeginX]、[BeginY] などのセルに親図形の座標を設定できます。</span><span class="sxs-lookup"><span data-stu-id="35be9-p101">Converts a point from local coordinates in a source shape to parent coordinates in a destination shape. You can use the LOCTOPAR function to set parent coordinates in cells, such as PinX, PinY, BeginX, and BeginY in a shape using another point from another coordinate system.</span></span> 
  
<span data-ttu-id="35be9-p102">変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。</span><span class="sxs-lookup"><span data-stu-id="35be9-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span> 
  
<span data-ttu-id="35be9-131">変換元図形と変換先図形の座標は、同じページ上になければなりません。</span><span class="sxs-lookup"><span data-stu-id="35be9-131">The source and destination coordinates must be on the same page.</span></span> 
  
<span data-ttu-id="35be9-132">変換先がページで、親図形がない場合、ページのローカル座標で結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="35be9-132">If the destination is a page, which has no parent, the result is expressed in the page's local coordinates.</span></span> 
  
## <a name="example"></a><span data-ttu-id="35be9-133">例</span><span class="sxs-lookup"><span data-stu-id="35be9-133">Example</span></span>

<span data-ttu-id="35be9-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span><span class="sxs-lookup"><span data-stu-id="35be9-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span></span> 
  
<span data-ttu-id="35be9-135">数式に関連付けられている図形のローカル Pin を Sheet.4 の親座標に変換します。</span><span class="sxs-lookup"><span data-stu-id="35be9-135">Converts the local pin of the shape associated with the formula to parent coordinates of Sheet.4.</span></span> 
  

