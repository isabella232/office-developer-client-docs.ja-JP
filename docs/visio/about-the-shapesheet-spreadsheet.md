---
title: シェイプシートのスプレッドシートについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251822
localization_priority: Normal
ms.assetid: f403890d-4a3a-bacc-53d7-1b9920b23639
description: Microsoft Visio のすべての要素 (図面、ページ、スタイル、図形、グループ、グループ内の図形やオブジェクト、マスター シェイプ、別のプログラムのオブジェクト、ガイド、ガイド点) には、それぞれのシェイプシートというスプレッドシートがあり、各オブジェクトについての情報が格納されています。このスプレッドシートには、高さ、幅、角度、色など、図形の外観や動作を決定する属性が含まれています。
ms.openlocfilehash: 37b2ae10b1f511197af5ccf739de91edb74e7819
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345174"
---
# <a name="about-the-shapesheet-spreadsheet"></a><span data-ttu-id="2f14a-104">シェイプシートのスプレッドシートについて</span><span class="sxs-lookup"><span data-stu-id="2f14a-104">About the ShapeSheet Spreadsheet</span></span>

<span data-ttu-id="2f14a-p102">Microsoft Visio のすべての要素 (図面、ページ、スタイル、図形、グループ、グループ内の図形やオブジェクト、マスター シェイプ、別のプログラムのオブジェクト、ガイド、ガイド点) には、それぞれのシェイプシートというスプレッドシートがあり、各オブジェクトについての情報が格納されています。このスプレッドシートには、高さ、幅、角度、色など、図形の外観や動作を決定する属性が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f14a-p102">Everything in Microsoft Visio, every document, page, style, shape, group, shape or object within a group, master, object from another program, guide, and guide point, has a ShapeSheet spreadsheet where information about that object is stored. This spreadsheet contains information such as height, width, angle, color, and other attributes that determine the shape's appearance and behavior.</span></span>
  
<span data-ttu-id="2f14a-p103">図形の開発者は、作成する図形の外観と動作を正確に設定する必要があります。図形の開発者は、シェイプシートで編集し、図形の既定の動作を変更して、機能を拡張できます。シェイプシートには、シェイプシート ウィンドウまたはプログラムからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-p103">As a shape developer, you need precise control over the appearance and behavior of the shapes you create. You can change a shape's default behavior and enhance what it can do by editing it in its ShapeSheet, which you can access in a ShapeSheet window or programmatically.</span></span>
  
## <a name="viewing-an-object-in-a-shapesheet-window"></a><span data-ttu-id="2f14a-109">[シェイプシート] ウィンドウでオブジェクトを表示する</span><span class="sxs-lookup"><span data-stu-id="2f14a-109">Viewing an object in a ShapeSheet window</span></span>

<span data-ttu-id="2f14a-110">Visio の図面ウィンドウと [シェイプシート] ウィンドウには、同じ図形に対して異なるビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-110">The Visio drawing window and ShapeSheet window are simply different views of the same shape.</span></span>
  
- <span data-ttu-id="2f14a-111">図面ウィンドウで図形を表示すると、図形はグラフィカルに描画されます。またシェイプシートの数式に従った動作を参照できます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-111">When you view a shape in a drawing window, you see it rendered graphically and behaving according to the formulas in its ShapeSheet.</span></span>
    
- <span data-ttu-id="2f14a-112">[シェイプシート] ウィンドウで図形を表示すると、図面ページでの図形の外観と動作を決定する、基本となる数式を参照できます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-112">When you view a shape in a ShapeSheet window, you see the underlying formulas that determine how it looks and behaves on the drawing page.</span></span>
    
<span data-ttu-id="2f14a-p104">[シェイプシート] ウィンドウと図面ウィンドウを同時に表示し、[シェイプシート] ウィンドウでセルを操作しながら図形の変更を図面ウィンドウで確認したり、逆の操作をしたりできます。たとえば、ポインターによって図形を移動すると、[Shape Transform] セクションにあるその図形の PinX 式と PinY 式が、図面ページ上の新しい位置を反映して変更されます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-p104">You can view a ShapeSheet window and a drawing window simultaneously and see the shape change in the drawing window as you manipulate cells in its ShapeSheet window or vice versa. For example, when you move the shape with the pointer, the shape's PinX and PinY formulas in the Shape Transform section change to reflect its new position on the drawing page.</span></span>
  
## <a name="structure-of-the-shapesheet-window"></a><span data-ttu-id="2f14a-115">[シェイプシート] ウィンドウの構造</span><span class="sxs-lookup"><span data-stu-id="2f14a-115">Structure of the ShapeSheet window</span></span>

<span data-ttu-id="2f14a-116">ShapeSheet は、図形の動作や外観の特定の側面 (ジオメトリや書式設定など) を制御するセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="2f14a-116">A ShapeSheet is divided into  *sections*  that control a particular aspect of a shape's behavior or appearance, for example, its geometry or its formatting.</span></span> <span data-ttu-id="2f14a-117">各セクションには、セルを含む 1 つ以上  *の*  行が  *含まれます*  。</span><span class="sxs-lookup"><span data-stu-id="2f14a-117">Each section contains one or more  *rows*  that contain  *cells*  .</span></span> <span data-ttu-id="2f14a-118">各セルには、数式とその結果 (セルの値と呼ばれます)、およびオプションのエラー情報を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-118">Each cell can contain a formula, its result (commonly called the cell value), and optional error information.</span></span> <span data-ttu-id="2f14a-119">数式は、セルに応じて、必須の場合とオプションの場合があります。</span><span class="sxs-lookup"><span data-stu-id="2f14a-119">A formula may be required or optional, depending on the particular cell.</span></span> <span data-ttu-id="2f14a-120">セルのデータ (数式や値など) はユーザーが定義できますが、多くの場合、図形のマスター シェイプまたはスタイル内にある対応するセルから継承されます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-120">A cell's data (for example, its formula or value) may be locally defined or, more often, inherited from the equivalent cell in the shape's master or style.</span></span> 
  
<span data-ttu-id="2f14a-121">次の例は、数式バーを示しています</span><span class="sxs-lookup"><span data-stu-id="2f14a-121">The following example shows the formula bar</span></span> ![数式バー](media/callout1_ZA01036259.gif)<span data-ttu-id="2f14a-123">、セクション</span><span class="sxs-lookup"><span data-stu-id="2f14a-123">, a section</span></span> ![section](media/callout2_ZA01036260.gif)<span data-ttu-id="2f14a-125">、セル</span><span class="sxs-lookup"><span data-stu-id="2f14a-125">, a cell</span></span> ![セル](media/callout3_ZA01036261.gif)<span data-ttu-id="2f14a-127">、および行</span><span class="sxs-lookup"><span data-stu-id="2f14a-127">, and a row</span></span> ![row](media/callout4_ZA01036262.gif) <span data-ttu-id="2f14a-129">を[シェイプシート] ウィンドウに表示します。</span><span class="sxs-lookup"><span data-stu-id="2f14a-129">in the ShapeSheet window.</span></span> 
  
![ShapeSheet ウィンドウ](media/ShpSheetRef_CA_02a_ZA07645861.gif)
  
<span data-ttu-id="2f14a-131">図形を描画すると、Visio では直線セグメントに接続された水平および垂直の位置のコレクションとしてその図形を記録します。</span><span class="sxs-lookup"><span data-stu-id="2f14a-131">When you draw a shape, Visio records the shape as a collection of horizontal and vertical locations connected with line segments.</span></span> <span data-ttu-id="2f14a-132">これらの場所 (頂点と呼ばれる) は、図形の [Geometry] セクションの X セルと Y セルに **記録** されます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-132">These locations (called vertices) are recorded in the X and Y cells of the shape's **Geometry** section.</span></span> <span data-ttu-id="2f14a-133">次の例に示すように、図形の [シェイプシート] ウィンドウの[Geometry] セクションで [X] セルと [Y] セルをクリックすると、図面ウィンドウで図形の頂点を強調表示する黒枠のボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-133">As shown in the following example, when you click the X and Y cells in the **Geometry** section of a shape's ShapeSheet window, you will see a black-bordered box highlighting the vertex on the shape in the drawing window.</span></span> 
  
![図面ウィンドウの図形上の頂点を強調表示する黒枠のボックス](media/ShpSheetRef_CA_01_ZA07645860.gif)
  
## <a name="editing-an-object-in-the-shapesheet-window"></a><span data-ttu-id="2f14a-135">[シェイプシート] ウィンドウでオブジェクトを編集する</span><span class="sxs-lookup"><span data-stu-id="2f14a-135">Editing an object in the ShapeSheet window</span></span>

<span data-ttu-id="2f14a-p107">[シェイプシート] ウィンドウがアクティブになると、リボンは、このウィンドウで作業するためのオプションが表示されるように変更されます。シェイプシートのセルを選択すると、オブジェクトの数式を入力または編集するための数式バーが表示されます。セルに直接数式を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-p107">When a ShapeSheet window is active, the ribbon changes to display options specific to working in this window. When you select a ShapeSheet cell, a formula bar appears, which you can use to enter and edit an object's formulas. Or, you can work directly in the cell.</span></span>
  
<span data-ttu-id="2f14a-139">[シェイプシート] ウィンドウでは、図形のシートにセクションを追加することで図面ページの図形に新しい特性を追加できます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-139">In a ShapeSheet window, you can add sections to a shape's sheet to add new characteristics to the shape on the drawing page.</span></span> <span data-ttu-id="2f14a-140">たとえば、[接続ポイント] セクションを追加 **して** 接続を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-140">For example, you can add a **Connection Points** section to create a connection.</span></span> <span data-ttu-id="2f14a-141">セクションが不要になった場合は、削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-141">When you no longer need a section, you can delete it.</span></span> 
  
<span data-ttu-id="2f14a-142">また、セクションに行を追加して、新しい式を保持したり、図形の外観を変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-142">You also can add rows to sections to hold additional formulas or to change a shape's appearance.</span></span> <span data-ttu-id="2f14a-143">たとえば、行を Geometry セクションに追加して、セグメントを図形に追加できます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-143">For example, you can add a row to a **Geometry** section to add a segment to a shape.</span></span> <span data-ttu-id="2f14a-144">同様に、不要になった行は削除できます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-144">Similarly, you can delete rows you no longer need.</span></span> 
  
<span data-ttu-id="2f14a-p110">セルには、数式または値のいずれでも表示できます。たとえば新しい数式を入力したり、既存の数式を編集したり、セルの数式の相互関係を確認する場合には、数式を表示します。セルの数式が評価されると、その結果として、値を受け取ります。セルの値を表示して評価の結果を確認できます。</span><span class="sxs-lookup"><span data-stu-id="2f14a-p110">You can display either formulas or values in cells. Display formulas when you are entering new formulas, editing existing formulas, or to see how formulas in cells relate to each other. A value is the result you get when Visio evaluates a cell's formula. You can display values in cells to see the result of an evaluation.</span></span>
  
## <a name="additional-shapesheet-references"></a><span data-ttu-id="2f14a-149">シェイプシートに関する参照情報</span><span class="sxs-lookup"><span data-stu-id="2f14a-149">Additional ShapeSheet references</span></span>

<span data-ttu-id="2f14a-150">シェイプシートの特定のセクション、行、またはセルの詳細については、このシェイプシートリファレンスの対応する [記事を参照してください](reference-visio-shapesheet.md)。</span><span class="sxs-lookup"><span data-stu-id="2f14a-150">For details on a particular section, row, or cell in the ShapeSheet, view the corresponding article in this [ShapeSheet Reference](reference-visio-shapesheet.md).</span></span>
  
<span data-ttu-id="2f14a-151">プログラムを使用してシェイプシートにアクセスする方法については、『Microsoft Visio オートメーション リファレンス』を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f14a-151">For details on programmatically accessing the ShapeSheet spreadsheet, see the Microsoft Visio Automation Reference.</span></span>
  

