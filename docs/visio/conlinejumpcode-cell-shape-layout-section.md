---
title: '[ConLineJumpCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: コネクタの飛び越し点の表示方法を指定します。
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805089"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="c9887-103">[ConLineJumpCode] セル ([図形レイアウト] セクション)</span><span class="sxs-lookup"><span data-stu-id="c9887-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="c9887-104">コネクタの飛び越し点の表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="c9887-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="c9887-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c9887-105">**Value**</span></span>|<span data-ttu-id="c9887-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="c9887-106">**Description**</span></span>|<span data-ttu-id="c9887-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="c9887-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9887-108">0</span><span class="sxs-lookup"><span data-stu-id="c9887-108">0</span></span>  <br/> |<span data-ttu-id="c9887-109">
          ページの指定に合わせます。[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックして、[**レイアウトと経路**] タブをクリックするとページの指定内容を参照できます。
</span><span class="sxs-lookup"><span data-stu-id="c9887-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="c9887-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="c9887-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="c9887-111">1</span><span class="sxs-lookup"><span data-stu-id="c9887-111">1</span></span>  <br/> |<span data-ttu-id="c9887-112">Never/なし</span><span class="sxs-lookup"><span data-stu-id="c9887-112">Never</span></span>  <br/> |<span data-ttu-id="c9887-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="c9887-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="c9887-114">2</span><span class="sxs-lookup"><span data-stu-id="c9887-114">2</span></span>  <br/> |<span data-ttu-id="c9887-115">Always/印刷/画面</span><span class="sxs-lookup"><span data-stu-id="c9887-115">Always</span></span>  <br/> |<span data-ttu-id="c9887-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="c9887-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="c9887-117">3</span><span class="sxs-lookup"><span data-stu-id="c9887-117">3</span></span>  <br/> |<span data-ttu-id="c9887-118">常に相手側に表示します。</span><span class="sxs-lookup"><span data-stu-id="c9887-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="c9887-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="c9887-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="c9887-120">4</span><span class="sxs-lookup"><span data-stu-id="c9887-120">4</span></span>  <br/> |<span data-ttu-id="c9887-121">
          どちらの側にも表示しません。
</span><span class="sxs-lookup"><span data-stu-id="c9887-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="c9887-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="c9887-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9887-123">注釈</span><span class="sxs-lookup"><span data-stu-id="c9887-123">Remarks</span></span>

<span data-ttu-id="c9887-124">設定できますでは、このセルの値、動的コネクタを**図形のデザイン**] で [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、**動作**をクリックして、[**コネクタ**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9887-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="c9887-125">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c9887-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9887-126">セル名:</span><span class="sxs-lookup"><span data-stu-id="c9887-126">Cell name:</span></span>  <br/> |<span data-ttu-id="c9887-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="c9887-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="c9887-128">プログラムから、インデックスによって [ConLineJumpCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c9887-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9887-129">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c9887-129">Section index:</span></span>  <br/> |<span data-ttu-id="c9887-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9887-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c9887-131">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c9887-131">Row index:</span></span>  <br/> |<span data-ttu-id="c9887-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="c9887-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="c9887-133">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c9887-133">Cell index:</span></span>  <br/> |<span data-ttu-id="c9887-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="c9887-134">**visSLOJumpCode**</span></span> <br/> |
   

