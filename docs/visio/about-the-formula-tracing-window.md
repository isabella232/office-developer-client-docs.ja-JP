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
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="7c6a1-103">[数式トレース] ウィンドウについて</span><span class="sxs-lookup"><span data-stu-id="7c6a1-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="7c6a1-104">[**数式トレース**] ウィンドウは、参照元セル (特定のセルに依存するセル) および参照先セル (特定のセルが依存するセル) の両方の相互依存に関する情報を図形作成者が表示できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="7c6a1-105">Microsoft Visio シェイプシートのセルには、値と数式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="7c6a1-106">数式は、他のセルを参照して、別のセルの値に基づいて1つのセルの値を計算することができます。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="7c6a1-107">ただし、複雑な図形を作成または維持している場合、数式は図面内の任意のセル、同じシェイプシートのセル、または図面内の別のオブジェクトに属するセルを参照できるので、これらの相互依存関係をすべて特定するのは困難です。たとえば、ページ、スタイル、マスターシェイプ、またはその他の図形です。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="7c6a1-108">[**数式トレース**] ウィンドウには、セルに加えた変更の影響を理解するのに役立つ情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="7c6a1-109">[数式トレース] ウィンドウを表示する</span><span class="sxs-lookup"><span data-stu-id="7c6a1-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="7c6a1-110">[**数式トレース**] ウィンドウを表示するには、[シェイプシート] ウィンドウをアクティブにして、[\* \* Design \* \*] タブの [**シェイプシートツール**] の下にある [**数式トレース**] グループで、[**ウィンドウの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="7c6a1-111">[**数式トレース**] ウィンドウは既定で [シェイプシート] ウィンドウに表示されますが、[**スタイルエクスプローラー** ] ウィンドウなどの他のアンカーされたシェイプシートウィンドウと一緒にドッキング、フローティング、または結合できるアンカーウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="7c6a1-112">参照元セルのトレース</span><span class="sxs-lookup"><span data-stu-id="7c6a1-112">Tracing dependent cells</span></span>

<span data-ttu-id="7c6a1-p103">特定のセルに依存するセルの一覧を表示するには、[シェイプシート] ウィンドウでそのセルを選択します。この例では、[Width] セルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![[Width] セルが選択されている](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="7c6a1-116">その依存セルを表示するには、[**式のトレース**] グループで、[参照先の**トレース**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-116">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="7c6a1-p104">[**数式トレース**] ウィンドウに、[Width] セルに依存するセルの一覧が表示されます。[**数式トレース**] ウィンドウで、一覧の中の任意のセルに移動するには、目的のセルのエントリをダブルクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-p104">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window. You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![[数式トレース] ウィンドウに [Width] セルに依存するすべてのセルが表示される](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="7c6a1-120">precendent セルのトレース</span><span class="sxs-lookup"><span data-stu-id="7c6a1-120">Tracing precendent cells</span></span>

<span data-ttu-id="7c6a1-p105">特定のセルが依存しているセルの一覧を表示するには、[シェイプシート] ウィンドウで該当のセルを選択します。この例では、[Geometry1.X2] セルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![geometry1.path セルが選択されている](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="7c6a1-124">参照元のセルを表示するには、[**式のトレース**] グループで、[**参照元のトレース**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-124">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="7c6a1-125">geometry1.path セルが依存しているすべてのセルの一覧が [**数式トレース**] ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="7c6a1-126">[**数式トレース**] ウィンドウで、一覧の中の任意のセルに移動するには、目的のセルのエントリをダブルクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="7c6a1-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![geometry1.path セルが依存しているすべてのセルが [数式トレース] ウィンドウに表示されます。](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

