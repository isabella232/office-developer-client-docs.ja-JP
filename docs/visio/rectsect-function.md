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
description: X に関連付けられている四角形のセクターを計算し、y、セクターを示す 0 ~ 4 の整数を返します。
ms.openlocfilehash: 1f35704cdb827c9c751f11593436c110755d7777
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806149"
---
# <a name="rectsect-function"></a><span data-ttu-id="dec5f-103">RECTSECT 関数</span><span class="sxs-lookup"><span data-stu-id="dec5f-103">RECTSECT Function</span></span>

<span data-ttu-id="dec5f-104">*X*および*y*に関連付けられている四角形のセクターを計算し、セクターを示す 0 ~ 4 の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="dec5f-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dec5f-105">構文</span><span class="sxs-lookup"><span data-stu-id="dec5f-105">Syntax</span></span>

<span data-ttu-id="dec5f-106">RECTSECT (* **幅** *、* **高さ** *、* * *x* * *、* * *y* * *、* **オプション** *)</span><span class="sxs-lookup"><span data-stu-id="dec5f-106">RECTSECT(** *width* **, ** *height* **, ** *x* **, ** *y* **, ** *option* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dec5f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dec5f-107">Parameters</span></span>

|<span data-ttu-id="dec5f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="dec5f-108">**Name**</span></span>|<span data-ttu-id="dec5f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="dec5f-109">**Required/Optional**</span></span>|<span data-ttu-id="dec5f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="dec5f-110">**Data Type**</span></span>|<span data-ttu-id="dec5f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="dec5f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dec5f-112">_width_</span><span class="sxs-lookup"><span data-stu-id="dec5f-112">_width_</span></span> <br/> |<span data-ttu-id="dec5f-113">必須</span><span class="sxs-lookup"><span data-stu-id="dec5f-113">Required</span></span>  <br/> |<span data-ttu-id="dec5f-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="dec5f-114">**String**</span></span> <br/> |<span data-ttu-id="dec5f-115">四角形の幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="dec5f-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="dec5f-116">_height_</span><span class="sxs-lookup"><span data-stu-id="dec5f-116">_height_</span></span> <br/> |<span data-ttu-id="dec5f-117">必須</span><span class="sxs-lookup"><span data-stu-id="dec5f-117">Required</span></span>  <br/> |<span data-ttu-id="dec5f-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="dec5f-118">**String**</span></span> <br/> |<span data-ttu-id="dec5f-119">四角形の高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="dec5f-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="dec5f-120">_x_</span><span class="sxs-lookup"><span data-stu-id="dec5f-120">_x_</span></span> <br/> |<span data-ttu-id="dec5f-121">必須</span><span class="sxs-lookup"><span data-stu-id="dec5f-121">Required</span></span>  <br/> |<span data-ttu-id="dec5f-122">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="dec5f-122">**String**</span></span> <br/> |<span data-ttu-id="dec5f-123">x 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="dec5f-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="dec5f-124">_y_</span><span class="sxs-lookup"><span data-stu-id="dec5f-124">_y_</span></span> <br/> |<span data-ttu-id="dec5f-125">必須</span><span class="sxs-lookup"><span data-stu-id="dec5f-125">Required</span></span>  <br/> |<span data-ttu-id="dec5f-126">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="dec5f-126">**String**</span></span> <br/> |<span data-ttu-id="dec5f-127">y 座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="dec5f-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="dec5f-128">_オプション_</span><span class="sxs-lookup"><span data-stu-id="dec5f-128">_option_</span></span> <br/> |<span data-ttu-id="dec5f-129">必須</span><span class="sxs-lookup"><span data-stu-id="dec5f-129">Required</span></span>  <br/> |<span data-ttu-id="dec5f-130">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="dec5f-130">**Boolean**</span></span> <br/> |<span data-ttu-id="dec5f-p101">対角線上の点の処理方法を指定します。対角線上の点に対して左右のセクターを使用するには、値を 0 に設定します。対角線上の点に対して上下のセクターを使用するには、値を 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="dec5f-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dec5f-134">注釈</span><span class="sxs-lookup"><span data-stu-id="dec5f-134">Remarks</span></span>

<span data-ttu-id="dec5f-135">四角形の*幅*と*高さ*、および四角形の中心点から点 (*x, y*) を持つことを検討してください。</span><span class="sxs-lookup"><span data-stu-id="dec5f-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="dec5f-136">中心点とその 4 つのセクターに分割するのには四角形の角を結ぶ対角線を描画します。</span><span class="sxs-lookup"><span data-stu-id="dec5f-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="dec5f-137">セクター 0 から 4 までは、中心点、右、上、左を表現し、それぞれの下します。</span><span class="sxs-lookup"><span data-stu-id="dec5f-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="dec5f-138">例</span><span class="sxs-lookup"><span data-stu-id="dec5f-138">Example</span></span>

<span data-ttu-id="dec5f-139">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span><span class="sxs-lookup"><span data-stu-id="dec5f-139">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="dec5f-140">4 を返します。</span><span class="sxs-lookup"><span data-stu-id="dec5f-140">Returns 4.</span></span> 
  

