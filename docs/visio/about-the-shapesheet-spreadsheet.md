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
ms.openlocfilehash: f443a596174ac4a555d53a271372e73367197da0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804736"
---
# <a name="about-the-shapesheet-spreadsheet"></a><span data-ttu-id="3c670-104">シェイプシート スプレッドシートについて</span><span class="sxs-lookup"><span data-stu-id="3c670-104">About the ShapeSheet Spreadsheet</span></span>

<span data-ttu-id="3c670-p102">Microsoft Visio のすべての要素 (図面、ページ、スタイル、図形、グループ、グループ内の図形やオブジェクト、マスター シェイプ、別のプログラムのオブジェクト、ガイド、ガイド点) には、それぞれのシェイプシートというスプレッドシートがあり、各オブジェクトについての情報が格納されています。このスプレッドシートには、高さ、幅、角度、色など、図形の外観や動作を決定する属性が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c670-p102">Everything in Microsoft Visio, every document, page, style, shape, group, shape or object within a group, master, object from another program, guide, and guide point, has a ShapeSheet spreadsheet where information about that object is stored. This spreadsheet contains information such as height, width, angle, color, and other attributes that determine the shape's appearance and behavior.</span></span>
  
<span data-ttu-id="3c670-p103">図形の開発者は、作成する図形の外観と動作を正確に設定する必要があります。図形の開発者は、シェイプシートで編集し、図形の既定の動作を変更して、機能を拡張できます。シェイプシートには、シェイプシート ウィンドウまたはプログラムからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3c670-p103">As a shape developer, you need precise control over the appearance and behavior of the shapes you create. You can change a shape's default behavior and enhance what it can do by editing it in its ShapeSheet, which you can access in a ShapeSheet window or programmatically.</span></span>
  
## <a name="viewing-an-object-in-a-shapesheet-window"></a><span data-ttu-id="3c670-109">[シェイプシート] ウィンドウでオブジェクトを表示する</span><span class="sxs-lookup"><span data-stu-id="3c670-109">Viewing an object in a ShapeSheet window</span></span>

<span data-ttu-id="3c670-110">Visio の図面ウィンドウと [シェイプシート] ウィンドウには、同じ図形に対して異なるビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c670-110">The Visio drawing window and ShapeSheet window are simply different views of the same shape.</span></span>
  
- <span data-ttu-id="3c670-111">図面ウィンドウで図形を表示すると、図形はグラフィカルに描画されます。またシェイプシートの数式に従った動作を参照できます。</span><span class="sxs-lookup"><span data-stu-id="3c670-111">When you view a shape in a drawing window, you see it rendered graphically and behaving according to the formulas in its ShapeSheet.</span></span>
    
- <span data-ttu-id="3c670-112">[シェイプシート] ウィンドウで図形を表示すると、図面ページでの図形の外観と動作を決定する、基本となる数式を参照できます。</span><span class="sxs-lookup"><span data-stu-id="3c670-112">When you view a shape in a ShapeSheet window, you see the underlying formulas that determine how it looks and behaves on the drawing page.</span></span>
    
<span data-ttu-id="3c670-p104">[シェイプシート] ウィンドウと図面ウィンドウを同時に表示し、[シェイプシート] ウィンドウでセルを操作しながら図形の変更を図面ウィンドウで確認したり、逆の操作をしたりできます。たとえば、ポインターによって図形を移動すると、[Shape Transform] セクションにあるその図形の PinX 式と PinY 式が、図面ページ上の新しい位置を反映して変更されます。</span><span class="sxs-lookup"><span data-stu-id="3c670-p104">You can view a ShapeSheet window and a drawing window simultaneously and see the shape change in the drawing window as you manipulate cells in its ShapeSheet window or vice versa. For example, when you move the shape with the pointer, the shape's PinX and PinY formulas in the Shape Transform section change to reflect its new position on the drawing page.</span></span>
  
## <a name="structure-of-the-shapesheet-window"></a><span data-ttu-id="3c670-115">[シェイプシート] ウィンドウの構造</span><span class="sxs-lookup"><span data-stu-id="3c670-115">Structure of the ShapeSheet window</span></span>

<span data-ttu-id="3c670-116">シェイプ シートは、座標や書式設定などの図形の動作や外観を特定の側面を制御する*セクション*に分割されます。</span><span class="sxs-lookup"><span data-stu-id="3c670-116">A ShapeSheet is divided into  *sections*  that control a particular aspect of a shape's behavior or appearance, for example, its geometry or its formatting.</span></span> <span data-ttu-id="3c670-117">各セクションには、*セル*を含む 1 つまたは複数の*行*が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c670-117">Each section contains one or more  *rows*  that contain  *cells*  .</span></span> <span data-ttu-id="3c670-118">各セルは、数式、その結果の (セルの値とよく呼ばれます) およびオプションのエラー情報を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3c670-118">Each cell can contain a formula, its result (commonly called the cell value), and optional error information.</span></span> <span data-ttu-id="3c670-119">必須またはオプションによっては、特定のセル、数式があります。</span><span class="sxs-lookup"><span data-stu-id="3c670-119">A formula may be required or optional, depending on the particular cell.</span></span> <span data-ttu-id="3c670-120">(たとえば、その数式または値) のセルのデータ、ローカルで定義されているかより多くの場合は、図形のマスター シェイプまたはスタイルに対応するセルから継承されています。</span><span class="sxs-lookup"><span data-stu-id="3c670-120">A cell's data (for example, its formula or value) may be locally defined or, more often, inherited from the equivalent cell in the shape's master or style.</span></span> 
  
<span data-ttu-id="3c670-121">次の例は、[シェイプシート] ウィンドウでの数式バー</span><span class="sxs-lookup"><span data-stu-id="3c670-121">The following example shows the formula bar</span></span> ![数値 1](media/callout1_ZA01036259.gif)<span data-ttu-id="3c670-123">、セクション</span><span class="sxs-lookup"><span data-stu-id="3c670-123">, a section</span></span> ![数値 2](media/callout2_ZA01036260.gif)<span data-ttu-id="3c670-125">、セル</span><span class="sxs-lookup"><span data-stu-id="3c670-125">, a cell</span></span> ![数値 3](media/callout3_ZA01036261.gif)<span data-ttu-id="3c670-127">、および行</span><span class="sxs-lookup"><span data-stu-id="3c670-127">, and a row</span></span> ![数値 4](media/callout4_ZA01036262.gif) <span data-ttu-id="3c670-129">を示しています。</span><span class="sxs-lookup"><span data-stu-id="3c670-129">in the ShapeSheet window.</span></span> 
  
![](media/ShpSheetRef_CA_02a_ZA07645861.gif)
  
<span data-ttu-id="3c670-130">図形を描画するときに、Visio は、直線セグメントに接続されている水平および垂直方向の位置のコレクションとして図形を記録します。</span><span class="sxs-lookup"><span data-stu-id="3c670-130">When you draw a shape, Visio records the shape as a collection of horizontal and vertical locations connected with line segments.</span></span> <span data-ttu-id="3c670-131">(頂点と呼ばれます)、これらの場所は、図形の [ **Geometry** ] セクションの X と Y のセルに記録されます。</span><span class="sxs-lookup"><span data-stu-id="3c670-131">These locations (called vertices) are recorded in the X and Y cells of the shape's **Geometry** section.</span></span> <span data-ttu-id="3c670-132">図形のシェイプ シート ウィンドウの [ **Geometry** ] セクションで、X と Y のセルをクリックしたときに、次の例では、ように、黒い枠線のボックスでの図面ウィンドウ内の図形の頂点を強調表示が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c670-132">As shown in the following example, when you click the X and Y cells in the **Geometry** section of a shape's ShapeSheet window, you will see a black-bordered box highlighting the vertex on the shape in the drawing window.</span></span> 
  
![](media/ShpSheetRef_CA_01_ZA07645860.gif)
  
## <a name="editing-an-object-in-the-shapesheet-window"></a><span data-ttu-id="3c670-133">[シェイプシート] ウィンドウでオブジェクトを編集する</span><span class="sxs-lookup"><span data-stu-id="3c670-133">Editing an object in the ShapeSheet window</span></span>

<span data-ttu-id="3c670-p107">[シェイプシート] ウィンドウがアクティブになると、リボンは、このウィンドウで作業するためのオプションが表示されるように変更されます。シェイプシートのセルを選択すると、オブジェクトの数式を入力または編集するための数式バーが表示されます。セルに直接数式を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="3c670-p107">When a ShapeSheet window is active, the ribbon changes to display options specific to working in this window. When you select a ShapeSheet cell, a formula bar appears, which you can use to enter and edit an object's formulas. Or, you can work directly in the cell.</span></span>
  
<span data-ttu-id="3c670-137">[シェイプ シート] ウィンドウで、図面ページ上の図形に新しい特性を追加する図形のシートにセクションを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="3c670-137">In a ShapeSheet window, you can add sections to a shape's sheet to add new characteristics to the shape on the drawing page.</span></span> <span data-ttu-id="3c670-138">たとえば、接続を作成する**接続ポイント**のセクションを追加できます。</span><span class="sxs-lookup"><span data-stu-id="3c670-138">For example, you can add a **Connection Points** section to create a connection.</span></span> <span data-ttu-id="3c670-139">セクション必要がなくなったときを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3c670-139">When you no longer need a section, you can delete it.</span></span> 
  
<span data-ttu-id="3c670-140">図形の外観を変更するのにはまたはその他の数式を保持するためのセクションに行を追加することも。</span><span class="sxs-lookup"><span data-stu-id="3c670-140">You also can add rows to sections to hold additional formulas or to change a shape's appearance.</span></span> <span data-ttu-id="3c670-141">たとえば、図形にセグメントを追加するのには **[Geometry** ] セクションに行を追加できます。</span><span class="sxs-lookup"><span data-stu-id="3c670-141">For example, you can add a row to a **Geometry** section to add a segment to a shape.</span></span> <span data-ttu-id="3c670-142">同様に、不要になった行を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3c670-142">Similarly, you can delete rows you no longer need.</span></span> 
  
<span data-ttu-id="3c670-p110">セルには、数式または値のいずれでも表示できます。たとえば新しい数式を入力したり、既存の数式を編集したり、セルの数式の相互関係を確認する場合には、数式を表示します。セルの数式が評価されると、その結果として、値を受け取ります。セルの値を表示して評価の結果を確認できます。</span><span class="sxs-lookup"><span data-stu-id="3c670-p110">You can display either formulas or values in cells. Display formulas when you are entering new formulas, editing existing formulas, or to see how formulas in cells relate to each other. A value is the result you get when Visio evaluates a cell's formula. You can display values in cells to see the result of an evaluation.</span></span>
  
## <a name="additional-shapesheet-references"></a><span data-ttu-id="3c670-147">シェイプシートに関する参照情報</span><span class="sxs-lookup"><span data-stu-id="3c670-147">Additional ShapeSheet references</span></span>

<span data-ttu-id="3c670-148">特定のセクション、行、または、[シェイプ シートのセルの詳細については、この[「シェイプ シート リファレンス](reference-visio-shapesheet.md)の対応する記事を表示します。</span><span class="sxs-lookup"><span data-stu-id="3c670-148">For details on a particular section, row, or cell in the ShapeSheet, view the corresponding article in this [ShapeSheet Reference](reference-visio-shapesheet.md).</span></span>
  
<span data-ttu-id="3c670-149">プログラムを使用してシェイプシートにアクセスする方法については、『Microsoft Visio オートメーション リファレンス』を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c670-149">For details on programmatically accessing the ShapeSheet spreadsheet, see the Microsoft Visio Automation Reference.</span></span>
  

