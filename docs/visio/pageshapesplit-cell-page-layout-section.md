---
title: '[PageShapeSplit] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: ページの図形が自動的に分割されるかどうかを示します。
ms.openlocfilehash: 7f1df0158cde6853c5518597c853cb56151eefbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805976"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="e5e2b-103">[PageShapeSplit] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="e5e2b-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="e5e2b-104">ページの図形が自動的に分割されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e5e2b-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="e5e2b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="e5e2b-105">**Value**</span></span>|<span data-ttu-id="e5e2b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="e5e2b-106">**Description**</span></span>|<span data-ttu-id="e5e2b-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="e5e2b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5e2b-108">0</span><span class="sxs-lookup"><span data-stu-id="e5e2b-108">0</span></span>  <br/> |<span data-ttu-id="e5e2b-109">図形は自動的に分割されません。</span><span class="sxs-lookup"><span data-stu-id="e5e2b-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="e5e2b-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="e5e2b-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="e5e2b-111">1</span><span class="sxs-lookup"><span data-stu-id="e5e2b-111">1</span></span>  <br/> |<span data-ttu-id="e5e2b-112">図形は自動的に分割されます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="e5e2b-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="e5e2b-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="e5e2b-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5e2b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e5e2b-114">Remarks</span></span>

<span data-ttu-id="e5e2b-p101">図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。図形に関する既定の設定は、図面の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e5e2b-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page levels. The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="e5e2b-118">アプリケーション レベルで分割を無効にするを有効または、 **Visio のオプション**] ダイアログ ボックスの [**詳細設定**] タブに**コネクタ分割を有効にする**設定を使用して、( **Office**ボタンをクリックし、 **Visio**の [**オプション**] をクリックしてタブをクリックし、[**詳細設定**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="e5e2b-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="e5e2b-119">図形レベルで分割を無効にするを有効またはは、[shapesplit] および [ShapeSplittable] セルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5e2b-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="e5e2b-120">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PageShapeSplit] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="e5e2b-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5e2b-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="e5e2b-121">Cell name:</span></span>  <br/> |<span data-ttu-id="e5e2b-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="e5e2b-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="e5e2b-123">プログラムから、インデックスによって [PageShapeSplit] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e5e2b-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5e2b-124">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e5e2b-124">Section index:</span></span>  <br/> |<span data-ttu-id="e5e2b-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e5e2b-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e5e2b-126">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e5e2b-126">Row index:</span></span>  <br/> |<span data-ttu-id="e5e2b-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e5e2b-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="e5e2b-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e5e2b-128">Cell index:</span></span>  <br/> |<span data-ttu-id="e5e2b-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="e5e2b-129">**visPLOSplit**</span></span> <br/> |
   

