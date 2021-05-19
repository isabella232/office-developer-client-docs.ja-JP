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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423896"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="e2951-103">[ShapePlowCode] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="e2951-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="e2951-104">図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e2951-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="e2951-105">**値**</span><span class="sxs-lookup"><span data-stu-id="e2951-105">**Value**</span></span>|<span data-ttu-id="e2951-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="e2951-106">**Description**</span></span>|<span data-ttu-id="e2951-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="e2951-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2951-108">0</span><span class="sxs-lookup"><span data-stu-id="e2951-108">0</span></span>  <br/> |<span data-ttu-id="e2951-109">ページの指定に従って移動します。</span><span class="sxs-lookup"><span data-stu-id="e2951-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="e2951-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="e2951-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="e2951-111">1</span><span class="sxs-lookup"><span data-stu-id="e2951-111">1</span></span>  <br/> |<span data-ttu-id="e2951-112">どの図形も移動しません。</span><span class="sxs-lookup"><span data-stu-id="e2951-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="e2951-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="e2951-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="e2951-114">2</span><span class="sxs-lookup"><span data-stu-id="e2951-114">2</span></span>  <br/> |<span data-ttu-id="e2951-115">すべての図形が移動します。</span><span class="sxs-lookup"><span data-stu-id="e2951-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="e2951-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="e2951-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2951-117">注釈</span><span class="sxs-lookup"><span data-stu-id="e2951-117">Remarks</span></span>

<span data-ttu-id="e2951-118">[動作] ダイアログ ボックスの [配置] タブで、特定の図形のこのセルの値を設定することもできます (図形が選択されている場合は、[開発] タブの[図形のデザイン] グループで、[動作] をクリックし、[配置] タブを **クリック** します)。  [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="e2951-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="e2951-119">図面ページのすべての  *図形に対*  してこの動作を設定するには、[ページ レイアウト] セクションの [PlowCode] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e2951-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="e2951-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlowCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2951-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2951-121">セル名 :</span><span class="sxs-lookup"><span data-stu-id="e2951-121">Cell name:</span></span>  <br/> |<span data-ttu-id="e2951-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="e2951-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="e2951-123">プログラムから、インデックスによって [ShapePlowCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2951-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2951-124">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e2951-124">Section index:</span></span>  <br/> |<span data-ttu-id="e2951-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e2951-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e2951-126">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e2951-126">Row index:</span></span>  <br/> |<span data-ttu-id="e2951-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="e2951-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="e2951-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e2951-128">Cell index:</span></span>  <br/> |<span data-ttu-id="e2951-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="e2951-129">**visSLOPlowCode**</span></span> <br/> |
   

