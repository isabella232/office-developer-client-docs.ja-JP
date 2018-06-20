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
ms.openlocfilehash: abb7208c2cfbd6b1423e091efc1d526f8b10b57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805698"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="b77c1-103">[LineJumpCode] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="b77c1-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="b77c1-104">飛び越し点を表示するコネクタを指定します。</span><span class="sxs-lookup"><span data-stu-id="b77c1-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="b77c1-105">**値**</span><span class="sxs-lookup"><span data-stu-id="b77c1-105">**Value**</span></span>|<span data-ttu-id="b77c1-106">**コネクタの飛び越し点を追加します。**</span><span class="sxs-lookup"><span data-stu-id="b77c1-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="b77c1-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="b77c1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b77c1-108">0</span><span class="sxs-lookup"><span data-stu-id="b77c1-108">0</span></span>  <br/> |<span data-ttu-id="b77c1-109">なし</span><span class="sxs-lookup"><span data-stu-id="b77c1-109">None</span></span>  <br/> |<span data-ttu-id="b77c1-110">**visPLOJumpNone**</span><span class="sxs-lookup"><span data-stu-id="b77c1-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="b77c1-111">1</span><span class="sxs-lookup"><span data-stu-id="b77c1-111">1</span></span>  <br/> |<span data-ttu-id="b77c1-112">横の線</span><span class="sxs-lookup"><span data-stu-id="b77c1-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="b77c1-113">**visPLOJumpHorizontal**</span><span class="sxs-lookup"><span data-stu-id="b77c1-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="b77c1-114">2</span><span class="sxs-lookup"><span data-stu-id="b77c1-114">2</span></span>  <br/> |<span data-ttu-id="b77c1-115">縦の線</span><span class="sxs-lookup"><span data-stu-id="b77c1-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="b77c1-116">**visPLOJumpVertical**</span><span class="sxs-lookup"><span data-stu-id="b77c1-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="b77c1-117">3</span><span class="sxs-lookup"><span data-stu-id="b77c1-117">3</span></span>  <br/> |<span data-ttu-id="b77c1-118">最後の経路</span><span class="sxs-lookup"><span data-stu-id="b77c1-118">Last routed line</span></span>  <br/> |<span data-ttu-id="b77c1-119">**visPLOJumpLastRouted**</span><span class="sxs-lookup"><span data-stu-id="b77c1-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="b77c1-120">4</span><span class="sxs-lookup"><span data-stu-id="b77c1-120">4</span></span>  <br/> |<span data-ttu-id="b77c1-121">最後に表示した線 ( *z*内の図形を上位の順)</span><span class="sxs-lookup"><span data-stu-id="b77c1-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="b77c1-122">**visPLOJumpDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="b77c1-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="b77c1-123">5</span><span class="sxs-lookup"><span data-stu-id="b77c1-123">5</span></span>  <br/> |<span data-ttu-id="b77c1-124">最初の行が表示されます ( *z*の一番下にある図形の順序)</span><span class="sxs-lookup"><span data-stu-id="b77c1-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="b77c1-125">**visPLOJumpReverseDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="b77c1-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b77c1-126">備考</span><span class="sxs-lookup"><span data-stu-id="b77c1-126">Remarks</span></span>

<span data-ttu-id="b77c1-127">**[ページ設定**] ダイアログ ボックスで、[**レイアウトと経路**] タブで、このセルの値を設定することもできます ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**レイアウトと経路**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="b77c1-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="b77c1-128">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineJumpCode] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="b77c1-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b77c1-129">セル名:</span><span class="sxs-lookup"><span data-stu-id="b77c1-129">Cell name:</span></span>  <br/> |<span data-ttu-id="b77c1-130">LineJumpCode</span><span class="sxs-lookup"><span data-stu-id="b77c1-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="b77c1-131">プログラムから、インデックスによって [LineJumpCode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b77c1-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b77c1-132">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b77c1-132">Section index:</span></span>  <br/> |<span data-ttu-id="b77c1-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b77c1-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b77c1-134">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b77c1-134">Row index:</span></span>  <br/> |<span data-ttu-id="b77c1-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b77c1-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b77c1-136">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b77c1-136">Cell index:</span></span>  <br/> |<span data-ttu-id="b77c1-137">**visPLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="b77c1-137">**visPLOJumpCode**</span></span> <br/> |
   

