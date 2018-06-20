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
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806415"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="fff8c-103">[ShapePlowCode] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="fff8c-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="fff8c-104">図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fff8c-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="fff8c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="fff8c-105">**Value**</span></span>|<span data-ttu-id="fff8c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="fff8c-106">**Description**</span></span>|<span data-ttu-id="fff8c-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="fff8c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fff8c-108">0</span><span class="sxs-lookup"><span data-stu-id="fff8c-108">0</span></span>  <br/> |<span data-ttu-id="fff8c-109">ページの指定に従って移動します。</span><span class="sxs-lookup"><span data-stu-id="fff8c-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="fff8c-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="fff8c-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="fff8c-111">1</span><span class="sxs-lookup"><span data-stu-id="fff8c-111">1</span></span>  <br/> |<span data-ttu-id="fff8c-112">どの図形も移動しません。</span><span class="sxs-lookup"><span data-stu-id="fff8c-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="fff8c-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="fff8c-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="fff8c-114">2</span><span class="sxs-lookup"><span data-stu-id="fff8c-114">2</span></span>  <br/> |<span data-ttu-id="fff8c-115">すべての図形が移動します。</span><span class="sxs-lookup"><span data-stu-id="fff8c-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="fff8c-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="fff8c-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fff8c-117">備考</span><span class="sxs-lookup"><span data-stu-id="fff8c-117">Remarks</span></span>

<span data-ttu-id="fff8c-118">**動作**] ダイアログ ボックスの [**配置**] タブで特定の図形のセルの値を設定することもできます (図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、**配置**] タブ)。</span><span class="sxs-lookup"><span data-stu-id="fff8c-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="fff8c-119">図面ページでこの動作を*すべて*の図形を設定するには、ページ レイアウト] セクションで [plowcode] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="fff8c-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="fff8c-120">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapePlowCode] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="fff8c-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fff8c-121">セル名 :</span><span class="sxs-lookup"><span data-stu-id="fff8c-121">Cell name:</span></span>  <br/> |<span data-ttu-id="fff8c-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="fff8c-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="fff8c-123">プログラムから、インデックスによって [ShapePlowCode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="fff8c-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fff8c-124">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fff8c-124">Section index:</span></span>  <br/> |<span data-ttu-id="fff8c-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fff8c-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fff8c-126">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fff8c-126">Row index:</span></span>  <br/> |<span data-ttu-id="fff8c-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="fff8c-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="fff8c-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fff8c-128">Cell index:</span></span>  <br/> |<span data-ttu-id="fff8c-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="fff8c-129">**visSLOPlowCode**</span></span> <br/> |
   

