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
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="dcb29-103">[ConLineJumpCode] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="dcb29-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="dcb29-104">コネクタの飛び越し点の表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="dcb29-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="dcb29-105">**値**</span><span class="sxs-lookup"><span data-stu-id="dcb29-105">**Value**</span></span>|<span data-ttu-id="dcb29-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="dcb29-106">**Description**</span></span>|<span data-ttu-id="dcb29-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="dcb29-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dcb29-108">0</span><span class="sxs-lookup"><span data-stu-id="dcb29-108">0</span></span>  <br/> |<span data-ttu-id="dcb29-109">ページで指定します。[**デザイン**] タブで、[**ページ設定**] で矢印をクリックし **、レイアウトと経路**] タブにページの仕様を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dcb29-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="dcb29-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="dcb29-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="dcb29-111">1</span><span class="sxs-lookup"><span data-stu-id="dcb29-111">1</span></span>  <br/> |<span data-ttu-id="dcb29-112">Never/なし</span><span class="sxs-lookup"><span data-stu-id="dcb29-112">Never</span></span>  <br/> |<span data-ttu-id="dcb29-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="dcb29-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="dcb29-114">2</span><span class="sxs-lookup"><span data-stu-id="dcb29-114">2</span></span>  <br/> |<span data-ttu-id="dcb29-115">Always/印刷/画面</span><span class="sxs-lookup"><span data-stu-id="dcb29-115">Always</span></span>  <br/> |<span data-ttu-id="dcb29-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="dcb29-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="dcb29-117">3</span><span class="sxs-lookup"><span data-stu-id="dcb29-117">3</span></span>  <br/> |<span data-ttu-id="dcb29-118">常に相手側に表示します。</span><span class="sxs-lookup"><span data-stu-id="dcb29-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="dcb29-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="dcb29-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="dcb29-120">4</span><span class="sxs-lookup"><span data-stu-id="dcb29-120">4</span></span>  <br/> |<span data-ttu-id="dcb29-121">どちらのコネクタに飛び越し点します。</span><span class="sxs-lookup"><span data-stu-id="dcb29-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="dcb29-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="dcb29-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcb29-123">備考</span><span class="sxs-lookup"><span data-stu-id="dcb29-123">Remarks</span></span>

<span data-ttu-id="dcb29-124">設定できますでは、このセルの値、動的コネクタを**図形のデザイン**] で [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、**動作**をクリックして、[**コネクタ**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcb29-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="dcb29-125">取得する、[ConLineJumpCode] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="dcb29-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcb29-126">セル名:</span><span class="sxs-lookup"><span data-stu-id="dcb29-126">Cell name:</span></span>  <br/> |<span data-ttu-id="dcb29-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="dcb29-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="dcb29-128">プログラムから、インデックスによって [ConLineJumpCode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="dcb29-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcb29-129">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dcb29-129">Section index:</span></span>  <br/> |<span data-ttu-id="dcb29-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dcb29-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dcb29-131">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dcb29-131">Row index:</span></span>  <br/> |<span data-ttu-id="dcb29-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="dcb29-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="dcb29-133">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dcb29-133">Cell index:</span></span>  <br/> |<span data-ttu-id="dcb29-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="dcb29-134">**visSLOJumpCode**</span></span> <br/> |
   

