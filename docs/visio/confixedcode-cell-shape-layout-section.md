---
title: '[ConFixedCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: コネクタの経路の変更方法を指定します。
ms.openlocfilehash: 448e721d8dd6e287c61488e28b875f76d0fa2977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805083"
---
# <a name="confixedcode-cell-shape-layout-section"></a><span data-ttu-id="047cc-103">[ConFixedCode] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="047cc-103">ConFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="047cc-104">コネクタの経路の変更方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="047cc-104">Determines when a connector reroutes.</span></span>
  
|<span data-ttu-id="047cc-105">**値**</span><span class="sxs-lookup"><span data-stu-id="047cc-105">**Value**</span></span>|<span data-ttu-id="047cc-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="047cc-106">**Description**</span></span>|<span data-ttu-id="047cc-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="047cc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="047cc-108">0</span><span class="sxs-lookup"><span data-stu-id="047cc-108">0</span></span>  <br/> |<span data-ttu-id="047cc-109">自由に経路変更します。</span><span class="sxs-lookup"><span data-stu-id="047cc-109">Reroute freely</span></span>  <br/> |<span data-ttu-id="047cc-110">**visSLOConFixedRerouteFreely**</span><span class="sxs-lookup"><span data-stu-id="047cc-110">**visSLOConFixedRerouteFreely**</span></span> <br/> |
|<span data-ttu-id="047cc-111">1</span><span class="sxs-lookup"><span data-stu-id="047cc-111">1</span></span>  <br/> |<span data-ttu-id="047cc-112">必要な (手動ルーティング) に応じて経路を変更します。</span><span class="sxs-lookup"><span data-stu-id="047cc-112">Reroute as needed (manual reroute)</span></span>  <br/> |<span data-ttu-id="047cc-113">**visSLOConFixedRerouteAsNeeded**</span><span class="sxs-lookup"><span data-stu-id="047cc-113">**visSLOConFixedRerouteAsNeeded**</span></span> <br/> |
|<span data-ttu-id="047cc-114">2</span><span class="sxs-lookup"><span data-stu-id="047cc-114">2</span></span>  <br/> |<span data-ttu-id="047cc-115">経路変更しません。</span><span class="sxs-lookup"><span data-stu-id="047cc-115">Never reroute</span></span>  <br/> |<span data-ttu-id="047cc-116">**visSLOConFixedRerouteNever**</span><span class="sxs-lookup"><span data-stu-id="047cc-116">**visSLOConFixedRerouteNever**</span></span> <br/> |
|<span data-ttu-id="047cc-117">3</span><span class="sxs-lookup"><span data-stu-id="047cc-117">3</span></span>  <br/> |<span data-ttu-id="047cc-118">交差時に経路変更します。</span><span class="sxs-lookup"><span data-stu-id="047cc-118">Reroute on crossover</span></span>  <br/> |<span data-ttu-id="047cc-119">**visSLOConFixedRerouteOnCrossover**</span><span class="sxs-lookup"><span data-stu-id="047cc-119">**visSLOConFixedRerouteOnCrossover**</span></span> <br/> |
|<span data-ttu-id="047cc-120">4</span><span class="sxs-lookup"><span data-stu-id="047cc-120">4</span></span>  <br/> |<span data-ttu-id="047cc-121">内部使用のみ。 </span><span class="sxs-lookup"><span data-stu-id="047cc-121">For internal use only</span></span>  <br/> |<span data-ttu-id="047cc-122">**visSLOConFixedByAlgFrom**</span><span class="sxs-lookup"><span data-stu-id="047cc-122">**visSLOConFixedByAlgFrom**</span></span> <br/> |
|<span data-ttu-id="047cc-123">5</span><span class="sxs-lookup"><span data-stu-id="047cc-123">5</span></span>  <br/> |<span data-ttu-id="047cc-124">内部使用のみ。 </span><span class="sxs-lookup"><span data-stu-id="047cc-124">For internal use only</span></span>  <br/> |<span data-ttu-id="047cc-125">**visSLOConFixedByAlgTo**</span><span class="sxs-lookup"><span data-stu-id="047cc-125">**visSLOConFixedByAlgTo**</span></span> <br/> |
|<span data-ttu-id="047cc-126">6</span><span class="sxs-lookup"><span data-stu-id="047cc-126">6</span></span>  <br/> |<span data-ttu-id="047cc-127">内部使用のみ。 </span><span class="sxs-lookup"><span data-stu-id="047cc-127">For internal use only</span></span>  <br/> |<span data-ttu-id="047cc-128">**visSLOConFixedByAlgFromTo**</span><span class="sxs-lookup"><span data-stu-id="047cc-128">**visSLOConFixedByAlgFromTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="047cc-129">備考</span><span class="sxs-lookup"><span data-stu-id="047cc-129">Remarks</span></span>

<span data-ttu-id="047cc-130">設定できますでは、このセルの値、動的コネクタを**図形のデザイン**] で [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、**動作**をクリックして、[**コネクタ**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="047cc-130">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="047cc-131">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ConFixedCode] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="047cc-131">To get a reference to the ConFixedCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="047cc-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="047cc-132">Cell name:</span></span>  <br/> |<span data-ttu-id="047cc-133">ConFixedCode</span><span class="sxs-lookup"><span data-stu-id="047cc-133">ConFixedCode</span></span>  <br/> |
   
<span data-ttu-id="047cc-134">プログラムから、インデックスによって [ConFixedCode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="047cc-134">To get a reference to the ConFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="047cc-135">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="047cc-135">Section index:</span></span>  <br/> |<span data-ttu-id="047cc-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="047cc-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="047cc-137">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="047cc-137">Row index:</span></span>  <br/> |<span data-ttu-id="047cc-138">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="047cc-138">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="047cc-139">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="047cc-139">Cell index:</span></span>  <br/> |<span data-ttu-id="047cc-140">**visSLOConFixedCode**</span><span class="sxs-lookup"><span data-stu-id="047cc-140">**visSLOConFixedCode**</span></span> <br/> |
   

