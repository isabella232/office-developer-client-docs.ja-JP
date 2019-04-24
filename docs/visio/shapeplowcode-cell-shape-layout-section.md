---
title: '[ShapePlowCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: 図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325607"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="e5ce9-103">[ShapePlowCode] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="e5ce9-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="e5ce9-104">図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5ce9-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="e5ce9-105">**値**</span><span class="sxs-lookup"><span data-stu-id="e5ce9-105">**Value**</span></span>|<span data-ttu-id="e5ce9-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="e5ce9-106">**Description**</span></span>|<span data-ttu-id="e5ce9-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="e5ce9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5ce9-108">.0</span><span class="sxs-lookup"><span data-stu-id="e5ce9-108">0</span></span>  <br/> |<span data-ttu-id="e5ce9-109">ページの指定に従って移動します。</span><span class="sxs-lookup"><span data-stu-id="e5ce9-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="e5ce9-110">**vissloん wdefault**</span><span class="sxs-lookup"><span data-stu-id="e5ce9-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="e5ce9-111">1-d</span><span class="sxs-lookup"><span data-stu-id="e5ce9-111">1</span></span>  <br/> |<span data-ttu-id="e5ce9-112">どの図形も移動しません。</span><span class="sxs-lookup"><span data-stu-id="e5ce9-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="e5ce9-113">**vissloの wnever**</span><span class="sxs-lookup"><span data-stu-id="e5ce9-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="e5ce9-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="e5ce9-114">2</span></span>  <br/> |<span data-ttu-id="e5ce9-115">すべての図形が移動します。</span><span class="sxs-lookup"><span data-stu-id="e5ce9-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="e5ce9-116">**visslo/always**</span><span class="sxs-lookup"><span data-stu-id="e5ce9-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5ce9-117">解説</span><span class="sxs-lookup"><span data-stu-id="e5ce9-117">Remarks</span></span>

<span data-ttu-id="e5ce9-118">このセルの値は、[**基本動作**] ダイアログボックスの [**配置**] タブで、特定の図形に対して設定することもできます (図形が選択されている状態で、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで、[**基本動作**] をクリックし、次にクリックします)。[**配置**] タブ)。</span><span class="sxs-lookup"><span data-stu-id="e5ce9-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="e5ce9-119">図面ページ上の*すべて*の図形に対してこの動作を設定するには、[ページレイアウト] セクションの [コード] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e5ce9-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="e5ce9-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlowCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5ce9-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5ce9-121">セル名 :</span><span class="sxs-lookup"><span data-stu-id="e5ce9-121">Cell name:</span></span>  <br/> |<span data-ttu-id="e5ce9-122">[shapeplowcode]</span><span class="sxs-lookup"><span data-stu-id="e5ce9-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="e5ce9-123">プログラムから、インデックスによって [ShapePlowCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5ce9-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5ce9-124">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e5ce9-124">Section index:</span></span>  <br/> |<span data-ttu-id="e5ce9-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e5ce9-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e5ce9-126">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e5ce9-126">Row index:</span></span>  <br/> |<span data-ttu-id="e5ce9-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="e5ce9-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="e5ce9-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e5ce9-128">Cell index:</span></span>  <br/> |<span data-ttu-id="e5ce9-129">**vissloの wコード**</span><span class="sxs-lookup"><span data-stu-id="e5ce9-129">**visSLOPlowCode**</span></span> <br/> |
   

