---
title: '[ShapePlaceFlip] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、配置可能な図形をページ上で反転および回転する方法、またはそのいずれかの方法を指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429279"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="ee7b2-103">[ShapePlaceFlip] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="ee7b2-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ee7b2-104">[**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに、配置可能な図形をページ上で反転および回転する方法、またはそのいずれかの方法を指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="ee7b2-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-105">**Value**</span></span>|<span data-ttu-id="ee7b2-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-106">**Description**</span></span>|<span data-ttu-id="ee7b2-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee7b2-108">.0</span><span class="sxs-lookup"><span data-stu-id="ee7b2-108">0</span></span>  <br/> |<span data-ttu-id="ee7b2-109">ページの既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-109">Use page default.</span></span>  <br/> |<span data-ttu-id="ee7b2-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="ee7b2-111">1 </span><span class="sxs-lookup"><span data-stu-id="ee7b2-111">1</span></span>  <br/> |<span data-ttu-id="ee7b2-112">水平方向に反転します。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="ee7b2-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="ee7b2-114">2 </span><span class="sxs-lookup"><span data-stu-id="ee7b2-114">2</span></span>  <br/> |<span data-ttu-id="ee7b2-115">垂直方向に反転します。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="ee7b2-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="ee7b2-117">4 </span><span class="sxs-lookup"><span data-stu-id="ee7b2-117">4</span></span>  <br/> |<span data-ttu-id="ee7b2-118">0 ～ 270°の範囲で 90°ずつ回転します。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="ee7b2-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="ee7b2-120">8 </span><span class="sxs-lookup"><span data-stu-id="ee7b2-120">8</span></span>  <br/> |<span data-ttu-id="ee7b2-121">反転しません。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="ee7b2-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee7b2-123">注釈</span><span class="sxs-lookup"><span data-stu-id="ee7b2-123">Remarks</span></span>

<span data-ttu-id="ee7b2-124">[ShapePlaceFlip] セルの値を使用すると、配置可能な図形の向きを、接続先となっている別の配置可能な図形に合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="ee7b2-125">図面ページ上の*すべて*の図形に対してこの動作を設定するには、[ページレイアウト] セクションの [配置] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="ee7b2-126">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlaceFlip] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee7b2-127">セル名:</span><span class="sxs-lookup"><span data-stu-id="ee7b2-127">Cell name:</span></span>  <br/> |<span data-ttu-id="ee7b2-128">[shapeplaceflip]</span><span class="sxs-lookup"><span data-stu-id="ee7b2-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="ee7b2-129">プログラムから、インデックスによって [ShapePlaceFlip] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ee7b2-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee7b2-130">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee7b2-130">Section index:</span></span>  <br/> |<span data-ttu-id="ee7b2-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ee7b2-132">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee7b2-132">Row index:</span></span>  <br/> |<span data-ttu-id="ee7b2-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="ee7b2-134">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee7b2-134">Cell index:</span></span>  <br/> |<span data-ttu-id="ee7b2-135">**vissloフェース eflip**</span><span class="sxs-lookup"><span data-stu-id="ee7b2-135">**visSLOPlaceFlip**</span></span> <br/> |
   

