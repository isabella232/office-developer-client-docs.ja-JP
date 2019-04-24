---
title: '[LineJumpCode] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: 飛び越し点を表示するコネクタを指定します。
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361118"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="6e393-103">[LineJumpCode] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="6e393-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="6e393-104">飛び越し点を表示するコネクタを指定します。</span><span class="sxs-lookup"><span data-stu-id="6e393-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="6e393-105">**値**</span><span class="sxs-lookup"><span data-stu-id="6e393-105">**Value**</span></span>|<span data-ttu-id="6e393-106">**飛び越し点を表示するコネクタ**</span><span class="sxs-lookup"><span data-stu-id="6e393-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="6e393-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="6e393-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6e393-108">.0</span><span class="sxs-lookup"><span data-stu-id="6e393-108">0</span></span>  <br/> |<span data-ttu-id="6e393-109">None</span><span class="sxs-lookup"><span data-stu-id="6e393-109">None</span></span>  <br/> |<span data-ttu-id="6e393-110">**visPLOJumpNone**</span><span class="sxs-lookup"><span data-stu-id="6e393-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="6e393-111">1-d</span><span class="sxs-lookup"><span data-stu-id="6e393-111">1</span></span>  <br/> |<span data-ttu-id="6e393-112">横の線</span><span class="sxs-lookup"><span data-stu-id="6e393-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="6e393-113">**visPLOJumpHorizontal**</span><span class="sxs-lookup"><span data-stu-id="6e393-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="6e393-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="6e393-114">2</span></span>  <br/> |<span data-ttu-id="6e393-115">縦の線</span><span class="sxs-lookup"><span data-stu-id="6e393-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="6e393-116">**visPLOJumpVertical**</span><span class="sxs-lookup"><span data-stu-id="6e393-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="6e393-117">1/3</span><span class="sxs-lookup"><span data-stu-id="6e393-117">3</span></span>  <br/> |<span data-ttu-id="6e393-118">最後の経路</span><span class="sxs-lookup"><span data-stu-id="6e393-118">Last routed line</span></span>  <br/> |<span data-ttu-id="6e393-119">**visPLOJumpLastRouted**</span><span class="sxs-lookup"><span data-stu-id="6e393-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="6e393-120">2/4</span><span class="sxs-lookup"><span data-stu-id="6e393-120">4</span></span>  <br/> |<span data-ttu-id="6e393-121">最後に表示された線 ( *z*オーダーの最上位の図形)</span><span class="sxs-lookup"><span data-stu-id="6e393-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="6e393-122">**visPLOJumpDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="6e393-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="6e393-123">5</span><span class="sxs-lookup"><span data-stu-id="6e393-123">5</span></span>  <br/> |<span data-ttu-id="6e393-124">最初に表示された行 ( *z*オーダーの一番下にある図形)</span><span class="sxs-lookup"><span data-stu-id="6e393-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="6e393-125">**visPLOJumpReverseDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="6e393-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e393-126">解説</span><span class="sxs-lookup"><span data-stu-id="6e393-126">Remarks</span></span>

<span data-ttu-id="6e393-127">このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="6e393-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="6e393-128">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineJumpCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6e393-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e393-129">セル名:</span><span class="sxs-lookup"><span data-stu-id="6e393-129">Cell name:</span></span>  <br/> |<span data-ttu-id="6e393-130">[linejumpcode]</span><span class="sxs-lookup"><span data-stu-id="6e393-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="6e393-131">プログラムから、インデックスによって [LineJumpCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e393-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e393-132">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6e393-132">Section index:</span></span>  <br/> |<span data-ttu-id="6e393-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6e393-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6e393-134">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6e393-134">Row index:</span></span>  <br/> |<span data-ttu-id="6e393-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="6e393-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="6e393-136">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6e393-136">Cell index:</span></span>  <br/> |<span data-ttu-id="6e393-137">**visPLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="6e393-137">**visPLOJumpCode**</span></span> <br/> |
   

