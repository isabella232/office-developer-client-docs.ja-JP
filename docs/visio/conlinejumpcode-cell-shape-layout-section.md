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
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421621"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="bfe4b-103">[ConLineJumpCode] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="bfe4b-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="bfe4b-104">コネクタの飛び越し点の表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfe4b-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="bfe4b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-105">**Value**</span></span>|<span data-ttu-id="bfe4b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-106">**Description**</span></span>|<span data-ttu-id="bfe4b-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bfe4b-108">.0</span><span class="sxs-lookup"><span data-stu-id="bfe4b-108">0</span></span>  <br/> |<span data-ttu-id="bfe4b-109">
          ページの指定に合わせます。[\*\*デザイン\*\*] タブの [\*\*ページ設定\*\*] グループの矢印をクリックして、[\*\*レイアウトと経路\*\*] タブをクリックするとページの指定内容を参照できます。
</span><span class="sxs-lookup"><span data-stu-id="bfe4b-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="bfe4b-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="bfe4b-111">1 </span><span class="sxs-lookup"><span data-stu-id="bfe4b-111">1</span></span>  <br/> |<span data-ttu-id="bfe4b-112">Never/なし</span><span class="sxs-lookup"><span data-stu-id="bfe4b-112">Never</span></span>  <br/> |<span data-ttu-id="bfe4b-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="bfe4b-114">2 </span><span class="sxs-lookup"><span data-stu-id="bfe4b-114">2</span></span>  <br/> |<span data-ttu-id="bfe4b-115">[Always/印刷/画面]</span><span class="sxs-lookup"><span data-stu-id="bfe4b-115">Always</span></span>  <br/> |<span data-ttu-id="bfe4b-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="bfe4b-117">3 </span><span class="sxs-lookup"><span data-stu-id="bfe4b-117">3</span></span>  <br/> |<span data-ttu-id="bfe4b-118">常に相手側に表示します。</span><span class="sxs-lookup"><span data-stu-id="bfe4b-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="bfe4b-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="bfe4b-120">4 </span><span class="sxs-lookup"><span data-stu-id="bfe4b-120">4</span></span>  <br/> |<span data-ttu-id="bfe4b-121">どちらの側にも表示しません。</span><span class="sxs-lookup"><span data-stu-id="bfe4b-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="bfe4b-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfe4b-123">注釈</span><span class="sxs-lookup"><span data-stu-id="bfe4b-123">Remarks</span></span>

<span data-ttu-id="bfe4b-124">このセルの値は、動的コネクタを選択し、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で [**基本動作**] をクリックし、[**コネクタ**] タブをクリックして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="bfe4b-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="bfe4b-125">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bfe4b-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfe4b-126">セル名:</span><span class="sxs-lookup"><span data-stu-id="bfe4b-126">Cell name:</span></span>  <br/> |<span data-ttu-id="bfe4b-127">[conlinejumpcode]</span><span class="sxs-lookup"><span data-stu-id="bfe4b-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="bfe4b-128">プログラムから、インデックスによって [ConLineJumpCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfe4b-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfe4b-129">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bfe4b-129">Section index:</span></span>  <br/> |<span data-ttu-id="bfe4b-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bfe4b-131">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bfe4b-131">Row index:</span></span>  <br/> |<span data-ttu-id="bfe4b-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="bfe4b-133">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bfe4b-133">Cell index:</span></span>  <br/> |<span data-ttu-id="bfe4b-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="bfe4b-134">**visSLOJumpCode**</span></span> <br/> |
   

