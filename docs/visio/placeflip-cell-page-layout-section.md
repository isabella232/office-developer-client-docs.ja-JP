---
title: '[PlaceFlip] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: '[レイアウトの構成] ダイアログ ボックスを使用するときに、配置可能な図形をページ上で反転または回転する方法を指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434299"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="bd04f-103">[PlaceFlip] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="bd04f-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="bd04f-104">[**レイアウトの構成**] ダイアログ ボックスを使用するときに、配置可能な図形をページ上で反転または回転する方法を指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="bd04f-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="bd04f-105">**値**</span><span class="sxs-lookup"><span data-stu-id="bd04f-105">**Value**</span></span>|<span data-ttu-id="bd04f-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="bd04f-106">**Description**</span></span>|<span data-ttu-id="bd04f-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="bd04f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd04f-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="bd04f-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="bd04f-109">既定値です。</span><span class="sxs-lookup"><span data-stu-id="bd04f-109">Default.</span></span> <span data-ttu-id="bd04f-110">反転しません。</span><span class="sxs-lookup"><span data-stu-id="bd04f-110">Do not flip.</span></span>  <br/> |<span data-ttu-id="bd04f-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="bd04f-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="bd04f-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="bd04f-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="bd04f-113">水平方向に反転します。</span><span class="sxs-lookup"><span data-stu-id="bd04f-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="bd04f-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="bd04f-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="bd04f-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="bd04f-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="bd04f-116">垂直方向に反転します。</span><span class="sxs-lookup"><span data-stu-id="bd04f-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="bd04f-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="bd04f-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="bd04f-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="bd04f-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="bd04f-119">90°単位で回転します。</span><span class="sxs-lookup"><span data-stu-id="bd04f-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="bd04f-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="bd04f-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="bd04f-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="bd04f-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="bd04f-122">反転しません。</span><span class="sxs-lookup"><span data-stu-id="bd04f-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="bd04f-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="bd04f-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd04f-124">注釈</span><span class="sxs-lookup"><span data-stu-id="bd04f-124">Remarks</span></span>

<span data-ttu-id="bd04f-p102">[PlaceFlip] セルの値を使用すると、配置可能な図形の向きを、接続先となっている隣接する配置可能な図形に合わせることができます。通常は、静的な接着を使用する図面をレイアウトする場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="bd04f-p102">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to. It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="bd04f-127">特定の図形に対してこの動作を設定するには、[Shape Layout] セクションで [ShapePlaceFlip] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="bd04f-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="bd04f-128">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PlaceFilp] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bd04f-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd04f-129">セル名:</span><span class="sxs-lookup"><span data-stu-id="bd04f-129">Cell name:</span></span>  <br/> |<span data-ttu-id="bd04f-130">[placeflip]</span><span class="sxs-lookup"><span data-stu-id="bd04f-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="bd04f-131">プログラムから、インデックスによって [PlaceFlip] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd04f-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd04f-132">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd04f-132">Section index:</span></span>  <br/> |<span data-ttu-id="bd04f-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bd04f-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bd04f-134">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd04f-134">Row index:</span></span>  <br/> |<span data-ttu-id="bd04f-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="bd04f-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="bd04f-136">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd04f-136">Cell index:</span></span>  <br/> |<span data-ttu-id="bd04f-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="bd04f-137">**visPLOPlaceFlip**</span></span> <br/> |
   

