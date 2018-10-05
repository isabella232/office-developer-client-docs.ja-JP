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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385327"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="08426-103">数式トレース ウィンドウについて</span><span class="sxs-lookup"><span data-stu-id="08426-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="08426-104">[**数式トレース**] ウィンドウは、参照元セル (特定のセルに依存するセル) および参照先セル (特定のセルが依存するセル) の両方の相互依存に関する情報を図形作成者が表示できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="08426-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="08426-105">Microsoft Visio シェイプ シートのセルには、値と数式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="08426-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="08426-106">数式を次が別のセルの値に基づいて 1 つのセルの値を計算するのには電源を提供する、他のセルへの参照。</span><span class="sxs-lookup"><span data-stu-id="08426-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="08426-107">作成するか、複雑な形状を維持する、ただし、ことができます同じシェイプ シート内のセルまたはセルを図面の別のオブジェクトに属することがあるかどうか数式は、図面内の任意のセルを参照できるため、これらすべての依存関係を識別することは困難。たとえば、ページ、スタイル、マスター、または別の図形です。</span><span class="sxs-lookup"><span data-stu-id="08426-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="08426-108">**数式トレース**] ウィンドウでは、セルに対して行う変更の意味合いを理解するのに役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="08426-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="08426-109">[数式トレース] ウィンドウを表示します。</span><span class="sxs-lookup"><span data-stu-id="08426-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="08426-110">シェイプ シート] ウィンドウをアクティブにして、[**シェイプ シート ツール**の [**数式トレース**] ウィンドウを表示するのには、\* \* デザイン \* \*] タブの [**数式トレース**] で、**ウィンドウの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="08426-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="08426-111">**数式トレース**] ウィンドウは、既定では、ドッキングされた [シェイプ シート] ウィンドウが表示されますが、アンカー ウィンドウのドッキング、フロート、またはマージできることを他の利用可能なシェイプ シート ウィンドウ、 **[スタイル エクスプ ローラー**ウィンドウなどでは。</span><span class="sxs-lookup"><span data-stu-id="08426-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="08426-112">参照元セルのトレース</span><span class="sxs-lookup"><span data-stu-id="08426-112">Tracing dependent cells</span></span>

<span data-ttu-id="08426-p103">特定のセルに依存するセルの一覧を表示するには、[シェイプシート] ウィンドウでそのセルを選択します。この例では、[Width] セルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="08426-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![[Width] セルが選択されています。](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="08426-116">[**数式トレース**] で、参照先のセルを表示するには、**参照先のトレース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="08426-116">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="08426-p104">[**数式トレース**] ウィンドウに、[Width] セルに依存するセルの一覧が表示されます。[**数式トレース**] ウィンドウで、一覧の中の任意のセルに移動するには、目的のセルのエントリをダブルクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="08426-p104">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window. You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![数式トレース] ウィンドウで、[Width] セルへの依存関係を持つすべてのセルが表示されます。](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="08426-120">Precendent セルのトレース</span><span class="sxs-lookup"><span data-stu-id="08426-120">Tracing precendent cells</span></span>

<span data-ttu-id="08426-p105">特定のセルが依存しているセルの一覧を表示するには、[シェイプシート] ウィンドウで該当のセルを選択します。この例では、[Geometry1.X2] セルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="08426-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![[Geometry1.x2] セルが選択されています。](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="08426-124">[**数式トレース**] で、その参照先のセルを表示するには、**参照元のトレース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="08426-124">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="08426-125">**数式トレース**] ウィンドウで、[geometry1.x2] セルが依存しているすべてのセルの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="08426-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="08426-126">**数式トレース**] ウィンドウ内のエントリをダブルクリックすると、リスト内の任意のセルに移動できます。</span><span class="sxs-lookup"><span data-stu-id="08426-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![[Geometry1.x2] セルが依存するすべてのセルは、[数式トレース] ウィンドウで表示されます。](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

