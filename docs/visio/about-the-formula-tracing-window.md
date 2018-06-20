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
description: '数式トレース] ウィンドウがセルの依存関係に関する情報を図形の開発者に提供するように設計されています: 参照先セル (特定のセルに依存するセル) および参照先セル (特定のセルが依存している)。'
ms.openlocfilehash: 316ac219f548b2459ea2d0ad8cece0f693957fcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804738"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="704fc-103">[数式トレース] ウィンドウについて</span><span class="sxs-lookup"><span data-stu-id="704fc-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="704fc-104">**数式トレース**] ウィンドウがセルの依存関係に関する情報を図形の開発者に提供するように設計されています: 参照先セル (特定のセルに依存するセル) および参照先セル (特定のセルが依存している)。</span><span class="sxs-lookup"><span data-stu-id="704fc-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="704fc-105">Microsoft Visio シェイプ シートのセルには、値と数式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="704fc-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="704fc-106">数式を次が別のセルの値に基づいて 1 つのセルの値を計算するのには電源を提供する、他のセルへの参照。</span><span class="sxs-lookup"><span data-stu-id="704fc-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="704fc-107">作成するか、複雑な形状を維持する、ただし、ことができます同じシェイプ シート内のセルまたはセルを図面の別のオブジェクトに属することがあるかどうか数式は、図面内の任意のセルを参照できるため、これらすべての依存関係を識別することは困難。たとえば、ページ、スタイル、マスター、または別の図形です。</span><span class="sxs-lookup"><span data-stu-id="704fc-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="704fc-108">**数式トレース**] ウィンドウでは、セルに対して行う変更の意味合いを理解するのに役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="704fc-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="704fc-109">[数式トレース] ウィンドウを表示します。</span><span class="sxs-lookup"><span data-stu-id="704fc-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="704fc-110">シェイプ シート] ウィンドウをアクティブにして、[**シェイプ シート ツール**の [**数式トレース**] ウィンドウを表示するのには、* * デザイン * *] タブの [**数式トレース**] で、**ウィンドウの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="704fc-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the ** Design ** tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="704fc-111">**数式トレース**] ウィンドウは、既定では、ドッキングされた [シェイプ シート] ウィンドウが表示されますが、アンカー ウィンドウのドッキング、フロート、またはマージできることを他の利用可能なシェイプ シート ウィンドウ、 **[スタイル エクスプ ローラー**ウィンドウなどでは。</span><span class="sxs-lookup"><span data-stu-id="704fc-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="704fc-112">従属セルをトレース</span><span class="sxs-lookup"><span data-stu-id="704fc-112">Tracing dependent cells</span></span>

<span data-ttu-id="704fc-p103">特定のセルに依存するセルの一覧を表示するには、[シェイプシート] ウィンドウでそのセルを選択します。この例では、[Width] セルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="704fc-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="704fc-115">[**数式トレース**] で、参照先のセルを表示するには、**参照先のトレース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="704fc-115">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="704fc-116">**数式トレース**] ウィンドウで、[Width] セルへの依存関係を持つすべてのセルの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="704fc-116">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="704fc-117">**数式トレース**] ウィンドウ内のエントリをダブルクリックすると、リスト内の任意のセルに移動できます。</span><span class="sxs-lookup"><span data-stu-id="704fc-117">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="704fc-118">Precendent セルのトレース</span><span class="sxs-lookup"><span data-stu-id="704fc-118">Tracing precendent cells</span></span>

<span data-ttu-id="704fc-p105">特定のセルが依存しているセルの一覧を表示するには、[シェイプシート] ウィンドウで該当のセルを選択します。この例では、[Geometry1.X2] セルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="704fc-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="704fc-121">[**数式トレース**] で、その参照先のセルを表示するには、**参照元のトレース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="704fc-121">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="704fc-122">**数式トレース**] ウィンドウで、[geometry1.x2] セルが依存しているすべてのセルの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="704fc-122">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="704fc-123">**数式トレース**] ウィンドウ内のエントリをダブルクリックすると、リスト内の任意のセルに移動できます。</span><span class="sxs-lookup"><span data-stu-id="704fc-123">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

