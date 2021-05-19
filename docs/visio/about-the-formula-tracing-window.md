---
title: '[数式トレース] ウィンドウについて'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: '[数式トレース] ウィンドウは、参照元セル (特定のセルに依存するセル) および参照先セル (特定のセルが依存するセル) の両方の相互依存に関する情報を図形作成者が表示できるように設計されています。'
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345325"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="b27b3-103">[数式トレース] ウィンドウについて</span><span class="sxs-lookup"><span data-stu-id="b27b3-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="b27b3-104">[**数式トレース**] ウィンドウは、参照元セル (特定のセルに依存するセル) および参照先セル (特定のセルが依存するセル) の両方の相互依存に関する情報を図形作成者が表示できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="b27b3-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="b27b3-105">Microsoft シェイプシートのセルにはVisio数式が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b27b3-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="b27b3-106">数式を使用すると、他のセルへの参照を取得して、別のセルの値に基づいて 1 つのセルの値を計算できます。</span><span class="sxs-lookup"><span data-stu-id="b27b3-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="b27b3-107">ただし、複雑な図形を作成または管理する場合、数式は図面内の任意のセル(同じシェイプシート内のセルか、ページ、スタイル、マスターシェイプ、または別の図形など)の別のオブジェクトに属するセルを参照することができるため、これらすべての相互依存関係を特定することは困難です。</span><span class="sxs-lookup"><span data-stu-id="b27b3-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="b27b3-108">[ **数式のトレース]** ウィンドウには、セルに加えた変更の影響を理解するのに役立つ情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b27b3-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="b27b3-109">数式トレース ウィンドウの表示</span><span class="sxs-lookup"><span data-stu-id="b27b3-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="b27b3-110">[数式トレース **] ウィンドウ** を表示するには、[シェイプシート] ウィンドウがアクティブな状態で、[\*\* デザイン \*\*]タブの [シェイプシート ツール] の [数式トレース] グループで、[ウィンドウの表示] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="b27b3-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="b27b3-111">既定では **、[Formula Tracing]** ウィンドウは ShapeSheet ウィンドウにドッキングされて表示されますが、固定されたウィンドウで、他の使用可能な固定シェイプシート ウィンドウ (スタイル エクスプローラー ウィンドウなど) とドッキング、浮動、または **結合できます。**</span><span class="sxs-lookup"><span data-stu-id="b27b3-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="b27b3-112">参照元セルのトレース</span><span class="sxs-lookup"><span data-stu-id="b27b3-112">Tracing dependent cells</span></span>

<span data-ttu-id="b27b3-p103">特定のセルに依存するセルの一覧を表示するには、[シェイプシート] ウィンドウでそのセルを選択します。この例では、[Width] セルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="b27b3-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![[幅] セルが選択されている](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="b27b3-116">依存セルを表示するには、[数式トレース] グループ **で**、[トレース依存] **をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="b27b3-116">To view its dependent cells, in the **Formula Tracing** group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="b27b3-p104">[**数式トレース**] ウィンドウに、[Width] セルに依存するセルの一覧が表示されます。[**数式トレース**] ウィンドウで、一覧の中の任意のセルに移動するには、目的のセルのエントリをダブルクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="b27b3-p104">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window. You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![[幅] セルに依存しているすべてのセルが [数式のトレース] ウィンドウに表示されます。](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="b27b3-120">設定済みセルのトレース</span><span class="sxs-lookup"><span data-stu-id="b27b3-120">Tracing precendent cells</span></span>

<span data-ttu-id="b27b3-p105">特定のセルが依存しているセルの一覧を表示するには、[シェイプシート] ウィンドウで該当のセルを選択します。この例では、[Geometry1.X2] セルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="b27b3-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![[Geometry1.X2] セルが選択されている](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="b27b3-124">その前のセルを表示するには、[数式のトレース] グループ **で**、[前例のトレース **] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="b27b3-124">To view its precedent cells, in the **Formula Tracing** group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="b27b3-125">[数式トレース] ウィンドウに、[Geometry1.X2] セルが依存しているすべてのセル **の一覧が表示** されます。</span><span class="sxs-lookup"><span data-stu-id="b27b3-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="b27b3-126">[**数式トレース**] ウィンドウで、一覧の中の任意のセルに移動するには、目的のセルのエントリをダブルクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="b27b3-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![[数式のトレース] ウィンドウに、[Geometry1.X2] セルが依存しているすべてのセルが表示されます。](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

