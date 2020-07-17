---
title: RECTSECT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: X と y に関連付けられた四角形のセクターを計算し、セクターを示す0から4までの整数を返します。
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160273"
---
# <a name="rectsect-function"></a><span data-ttu-id="1cf88-103">RECTSECT 関数</span><span class="sxs-lookup"><span data-stu-id="1cf88-103">RECTSECT Function</span></span>

<span data-ttu-id="1cf88-104">*X*と*y*に関連付けられた四角形のセクターを計算し、セクターを示す0から4までの整数を返します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1cf88-105">構文</span><span class="sxs-lookup"><span data-stu-id="1cf88-105">Syntax</span></span>

<span data-ttu-id="1cf88-106">RECTSECT (***width***、 ***height***、 ***x***、 ***y***、 ***option*** )</span><span class="sxs-lookup"><span data-stu-id="1cf88-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1cf88-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1cf88-107">Parameters</span></span>

|<span data-ttu-id="1cf88-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="1cf88-108">**Name**</span></span>|<span data-ttu-id="1cf88-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="1cf88-109">**Required/Optional**</span></span>|<span data-ttu-id="1cf88-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="1cf88-110">**Data Type**</span></span>|<span data-ttu-id="1cf88-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="1cf88-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1cf88-112">_width_</span><span class="sxs-lookup"><span data-stu-id="1cf88-112">_width_</span></span> <br/> |<span data-ttu-id="1cf88-113">必須</span><span class="sxs-lookup"><span data-stu-id="1cf88-113">Required</span></span>  <br/> |<span data-ttu-id="1cf88-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1cf88-114">**String**</span></span> <br/> |<span data-ttu-id="1cf88-115">四角形の幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="1cf88-116">_height_</span><span class="sxs-lookup"><span data-stu-id="1cf88-116">_height_</span></span> <br/> |<span data-ttu-id="1cf88-117">必須</span><span class="sxs-lookup"><span data-stu-id="1cf88-117">Required</span></span>  <br/> |<span data-ttu-id="1cf88-118">**String**</span><span class="sxs-lookup"><span data-stu-id="1cf88-118">**String**</span></span> <br/> |<span data-ttu-id="1cf88-119">四角形の高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="1cf88-120">_x_</span><span class="sxs-lookup"><span data-stu-id="1cf88-120">_x_</span></span> <br/> |<span data-ttu-id="1cf88-121">必須</span><span class="sxs-lookup"><span data-stu-id="1cf88-121">Required</span></span>  <br/> |<span data-ttu-id="1cf88-122">**String**</span><span class="sxs-lookup"><span data-stu-id="1cf88-122">**String**</span></span> <br/> |<span data-ttu-id="1cf88-123">x 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="1cf88-124">_y_</span><span class="sxs-lookup"><span data-stu-id="1cf88-124">_y_</span></span> <br/> |<span data-ttu-id="1cf88-125">必須</span><span class="sxs-lookup"><span data-stu-id="1cf88-125">Required</span></span>  <br/> |<span data-ttu-id="1cf88-126">**String**</span><span class="sxs-lookup"><span data-stu-id="1cf88-126">**String**</span></span> <br/> |<span data-ttu-id="1cf88-127">y 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="1cf88-128">_方法_</span><span class="sxs-lookup"><span data-stu-id="1cf88-128">_option_</span></span> <br/> |<span data-ttu-id="1cf88-129">必須</span><span class="sxs-lookup"><span data-stu-id="1cf88-129">Required</span></span>  <br/> |<span data-ttu-id="1cf88-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1cf88-130">**Boolean**</span></span> <br/> |<span data-ttu-id="1cf88-p101">対角線上の点の処理方法を指定します。対角線上の点に対して左右のセクターを使用するには、値を 0 に設定します。対角線上の点に対して上下のセクターを使用するには、値を 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cf88-134">備考</span><span class="sxs-lookup"><span data-stu-id="1cf88-134">Remarks</span></span>

<span data-ttu-id="1cf88-135">*幅*と*高さ*を持つ四角形と、四角形の中心点からの点 (*x, y*) を考慮します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="1cf88-136">四角形の角を結ぶ対角線を描画し、四角形を 4 つのセクターに分割して、中心点を示します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="1cf88-137">セクター 0 ～ 4 は、それぞれ中心点、右、上、左、下を表します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![セクター 0 ~ 4 は、それぞれ中心点、右、上、左、および下を表します。](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="1cf88-139">例</span><span class="sxs-lookup"><span data-stu-id="1cf88-139">Example</span></span>

<span data-ttu-id="1cf88-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span><span class="sxs-lookup"><span data-stu-id="1cf88-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="1cf88-141">4 を返します。</span><span class="sxs-lookup"><span data-stu-id="1cf88-141">Returns 4.</span></span> 
  

