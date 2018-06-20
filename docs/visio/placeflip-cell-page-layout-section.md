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
description: どのように配置可能な図形を指定する反転または回転して、ページ レイアウトの構成] ダイアログ ボックスを使用する場合 ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: fb16849c7a496a4277133c68453d94d6fd2e67f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805991"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="36b12-103">[PlaceFlip] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="36b12-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="36b12-104">どのように配置可能な図形を指定する反転または回転して、ページ**レイアウトの構成**] ダイアログ ボックスを使用する場合 ([**デザイン**] タブの [**レイアウト**] で、**ページの再レイアウト**] をクリックし、**他のレイアウト オプション**をクリックし、)。</span><span class="sxs-lookup"><span data-stu-id="36b12-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="36b12-105">**値**</span><span class="sxs-lookup"><span data-stu-id="36b12-105">**Value**</span></span>|<span data-ttu-id="36b12-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="36b12-106">**Description**</span></span>|<span data-ttu-id="36b12-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="36b12-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36b12-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="36b12-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="36b12-p101">既定値です。反転しません。</span><span class="sxs-lookup"><span data-stu-id="36b12-p101">Default. Do not flip.</span></span>  <br/> |<span data-ttu-id="36b12-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="36b12-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="36b12-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="36b12-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="36b12-113">水平方向に反転します。</span><span class="sxs-lookup"><span data-stu-id="36b12-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="36b12-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="36b12-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="36b12-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="36b12-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="36b12-116">垂直方向に反転します。</span><span class="sxs-lookup"><span data-stu-id="36b12-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="36b12-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="36b12-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="36b12-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="36b12-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="36b12-119">90°単位で回転します。</span><span class="sxs-lookup"><span data-stu-id="36b12-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="36b12-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="36b12-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="36b12-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="36b12-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="36b12-122">反転しません。</span><span class="sxs-lookup"><span data-stu-id="36b12-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="36b12-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="36b12-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36b12-124">注釈</span><span class="sxs-lookup"><span data-stu-id="36b12-124">Remarks</span></span>

<span data-ttu-id="36b12-p102">[PlaceFlip] セルの値を使用すると、配置可能な図形の向きを、接続先となっている隣接する配置可能な図形に合わせることができます。通常は、静的な接着を使用する図面をレイアウトする場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="36b12-p102">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to. It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="36b12-127">特定の図形に対してこの動作を設定するには、[Shape Layout] セクションで [ShapePlaceFlip] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="36b12-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="36b12-128">取得する、[PlaceFlip] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="36b12-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36b12-129">セル名:</span><span class="sxs-lookup"><span data-stu-id="36b12-129">Cell name:</span></span>  <br/> |<span data-ttu-id="36b12-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="36b12-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="36b12-131">プログラムから、インデックスによって [PlaceFlip] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="36b12-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36b12-132">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="36b12-132">Section index:</span></span>  <br/> |<span data-ttu-id="36b12-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="36b12-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="36b12-134">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="36b12-134">Row index:</span></span>  <br/> |<span data-ttu-id="36b12-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="36b12-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="36b12-136">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="36b12-136">Cell index:</span></span>  <br/> |<span data-ttu-id="36b12-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="36b12-137">**visPLOPlaceFlip**</span></span> <br/> |
   

