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
ms.openlocfilehash: b2b9cde309c720493f0e46962b2fe6c2e79545d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284463"
---
# <a name="confixedcode-cell-shape-layout-section"></a><span data-ttu-id="08c80-103">[ConFixedCode] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="08c80-103">ConFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="08c80-104">コネクタの経路の変更方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="08c80-104">Determines when a connector reroutes.</span></span>
  
|<span data-ttu-id="08c80-105">**値**</span><span class="sxs-lookup"><span data-stu-id="08c80-105">**Value**</span></span>|<span data-ttu-id="08c80-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="08c80-106">**Description**</span></span>|<span data-ttu-id="08c80-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="08c80-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="08c80-108">.0</span><span class="sxs-lookup"><span data-stu-id="08c80-108">0</span></span>  <br/> |<span data-ttu-id="08c80-109">自由に経路を変更します。</span><span class="sxs-lookup"><span data-stu-id="08c80-109">Reroute freely</span></span>  <br/> |<span data-ttu-id="08c80-110">**visSLOConFixedRerouteFreely**</span><span class="sxs-lookup"><span data-stu-id="08c80-110">**visSLOConFixedRerouteFreely**</span></span> <br/> |
|<span data-ttu-id="08c80-111">1-d</span><span class="sxs-lookup"><span data-stu-id="08c80-111">1</span></span>  <br/> |<span data-ttu-id="08c80-112">必要に応じて経路を再設定します (手動による変更)。</span><span class="sxs-lookup"><span data-stu-id="08c80-112">Reroute as needed (manual reroute)</span></span>  <br/> |<span data-ttu-id="08c80-113">**visSLOConFixedRerouteAsNeeded**</span><span class="sxs-lookup"><span data-stu-id="08c80-113">**visSLOConFixedRerouteAsNeeded**</span></span> <br/> |
|<span data-ttu-id="08c80-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="08c80-114">2</span></span>  <br/> |<span data-ttu-id="08c80-115">経路変更しません。</span><span class="sxs-lookup"><span data-stu-id="08c80-115">Never reroute</span></span>  <br/> |<span data-ttu-id="08c80-116">**visSLOConFixedRerouteNever**</span><span class="sxs-lookup"><span data-stu-id="08c80-116">**visSLOConFixedRerouteNever**</span></span> <br/> |
|<span data-ttu-id="08c80-117">1/3</span><span class="sxs-lookup"><span data-stu-id="08c80-117">3</span></span>  <br/> |<span data-ttu-id="08c80-118">交差時に経路を変更します。</span><span class="sxs-lookup"><span data-stu-id="08c80-118">Reroute on crossover</span></span>  <br/> |<span data-ttu-id="08c80-119">**visSLOConFixedRerouteOnCrossover**</span><span class="sxs-lookup"><span data-stu-id="08c80-119">**visSLOConFixedRerouteOnCrossover**</span></span> <br/> |
|<span data-ttu-id="08c80-120">2/4</span><span class="sxs-lookup"><span data-stu-id="08c80-120">4</span></span>  <br/> |<span data-ttu-id="08c80-121">システム内部でのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="08c80-121">For internal use only</span></span>  <br/> |<span data-ttu-id="08c80-122">**visSLOConFixedByAlgFrom**</span><span class="sxs-lookup"><span data-stu-id="08c80-122">**visSLOConFixedByAlgFrom**</span></span> <br/> |
|<span data-ttu-id="08c80-123">5</span><span class="sxs-lookup"><span data-stu-id="08c80-123">5</span></span>  <br/> |<span data-ttu-id="08c80-124">システム内部でのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="08c80-124">For internal use only</span></span>  <br/> |<span data-ttu-id="08c80-125">**visSLOConFixedByAlgTo**</span><span class="sxs-lookup"><span data-stu-id="08c80-125">**visSLOConFixedByAlgTo**</span></span> <br/> |
|<span data-ttu-id="08c80-126">シックス</span><span class="sxs-lookup"><span data-stu-id="08c80-126">6</span></span>  <br/> |<span data-ttu-id="08c80-127">システム内部でのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="08c80-127">For internal use only</span></span>  <br/> |<span data-ttu-id="08c80-128">**visSLOConFixedByAlgFromTo**</span><span class="sxs-lookup"><span data-stu-id="08c80-128">**visSLOConFixedByAlgFromTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08c80-129">解説</span><span class="sxs-lookup"><span data-stu-id="08c80-129">Remarks</span></span>

<span data-ttu-id="08c80-130">このセルの値は、動的コネクタを選択し、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で [**基本動作**] をクリックし、[**コネクタ**] タブをクリックして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="08c80-130">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="08c80-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConFixedCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="08c80-131">To get a reference to the ConFixedCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08c80-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="08c80-132">Cell name:</span></span>  <br/> |<span data-ttu-id="08c80-133">[confixedcode]</span><span class="sxs-lookup"><span data-stu-id="08c80-133">ConFixedCode</span></span>  <br/> |
   
<span data-ttu-id="08c80-134">プログラムから、インデックスによって [ConFixedCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="08c80-134">To get a reference to the ConFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08c80-135">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="08c80-135">Section index:</span></span>  <br/> |<span data-ttu-id="08c80-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="08c80-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="08c80-137">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="08c80-137">Row index:</span></span>  <br/> |<span data-ttu-id="08c80-138">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="08c80-138">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="08c80-139">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="08c80-139">Cell index:</span></span>  <br/> |<span data-ttu-id="08c80-140">**visslo# xedcode**</span><span class="sxs-lookup"><span data-stu-id="08c80-140">**visSLOConFixedCode**</span></span> <br/> |
   

