---
title: 数式について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: 図形のアクションを制御するには、必要な動作を定義する数式を記述します。セルの数式を編集すると、そのセルの値を変更し、結果的に特定の図形の動作を変更できます。たとえば、[Shape Transform] セクションの [Height] セルに含まれる数式を変更すると、その図形の高さを変更できます。
ms.openlocfilehash: 7df5ffe4d3dc32bcd5209bde353c39a92c7d422b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804728"
---
# <a name="about-formulas"></a><span data-ttu-id="616d0-105">数式について</span><span class="sxs-lookup"><span data-stu-id="616d0-105">About Formulas</span></span>

<span data-ttu-id="616d0-p102">図形のアクションを制御するには、必要な動作を定義する数式を記述します。セルの数式を編集すると、そのセルの値を変更し、結果的に特定の図形の動作を変更できます。たとえば、[Shape Transform] セクションの [Height] セルに含まれる数式を変更すると、その図形の高さを変更できます。</span><span class="sxs-lookup"><span data-stu-id="616d0-p102">The key to controlling shape actions is to write formulas that define the behavior you want. You can edit a cell's formula to change the value of the cell and, as a result, change a particular shape's behavior. For example, the Height cell in the Shape Transform section contains a formula that you can change to alter the shape's height.</span></span>
  
<span data-ttu-id="616d0-p103">Microsoft Visio の数式は、多くの点で一般的なスプレッドシートの数式と類似しています。Visio では、数値や簡単なセル参照なども含め、セル内の情報はすべて数式として扱われます。</span><span class="sxs-lookup"><span data-stu-id="616d0-p103">Microsoft Visio formulas are similar to typical spreadsheet formulas in many ways. Visio regards anything in a cell, even if it is a numeric value or simple cell reference, as a formula.</span></span>
  
<span data-ttu-id="616d0-p104">セル内の数式は、マスター シェイプまたはスタイルの対応するセルから継承することも、ユーザーが独自に定義することもできます。数式が評価されると、その結果がセルに適した値と単位に変換されます。[シェイプシート] ウィンドウでは、セルの内容を数式または値で表示できます。</span><span class="sxs-lookup"><span data-stu-id="616d0-p104">A formula in a cell can be inherited from the equivalent cell of a master or a style or defined locally. Visio evaluates the formula and then converts the results to an appropriate value and appropriate units for the cell. In a ShapeSheet window, you can display cell contents as either formulas or values.</span></span>
  
## <a name="elements-of-a-formula"></a><span data-ttu-id="616d0-114">数式の要素</span><span class="sxs-lookup"><span data-stu-id="616d0-114">Elements of a formula</span></span>

<span data-ttu-id="616d0-p105">数式の先頭には、常に等号が自動的に挿入されます。数式には次の要素を使用できます。</span><span class="sxs-lookup"><span data-stu-id="616d0-p105">A formula always starts with an equal sign, which is inserted automatically. A formula can include any of the following elements:</span></span>
  
- <span data-ttu-id="616d0-117">数値</span><span class="sxs-lookup"><span data-stu-id="616d0-117">Numbers</span></span>
    
- <span data-ttu-id="616d0-118">座標</span><span class="sxs-lookup"><span data-stu-id="616d0-118">Coordinates</span></span>
    
- <span data-ttu-id="616d0-119">ブール値</span><span class="sxs-lookup"><span data-stu-id="616d0-119">Boolean values</span></span>
    
- <span data-ttu-id="616d0-120">演算子</span><span class="sxs-lookup"><span data-stu-id="616d0-120">Operators</span></span>
    
- <span data-ttu-id="616d0-121">関数</span><span class="sxs-lookup"><span data-stu-id="616d0-121">Functions</span></span>
    
- <span data-ttu-id="616d0-122">文字列</span><span class="sxs-lookup"><span data-stu-id="616d0-122">Strings</span></span>
    
- <span data-ttu-id="616d0-123">セル参照</span><span class="sxs-lookup"><span data-stu-id="616d0-123">Cell references</span></span>
    
- <span data-ttu-id="616d0-124">単位</span><span class="sxs-lookup"><span data-stu-id="616d0-124">Units of measure</span></span>
    
## <a name="default-formulas"></a><span data-ttu-id="616d0-125">既定の数式</span><span class="sxs-lookup"><span data-stu-id="616d0-125">Default formulas</span></span>

<span data-ttu-id="616d0-p106">図形を作成すると、その図形に関する既定の数式が作成されます。既定の数式を確認するには、単純な図形 (四角形、楕円、直線など) を描画し、その [シェイプシート] ウィンドウを開きます。[シェイプシート] ウィンドウを開くには、図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**シェイプシートの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="616d0-p106">When you create a shape, Visio creates formulas for it by default. To see what the default formulas are, draw a simple shape (such as a rectangle, ellipse, or straight line) and open its ShapeSheet window (on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, click **Show ShapeSheet**).</span></span>
  
## <a name="inherited-formulas"></a><span data-ttu-id="616d0-128">継承された数式</span><span class="sxs-lookup"><span data-stu-id="616d0-128">Inherited formulas</span></span>

<span data-ttu-id="616d0-p107">Visio では、可能である場合には数式が継承されます。インスタンスにすべての数式のローカル コピーを作成するのではなく、インスタンスは図面ステンシルのマスター シェイプから数式を継承し、図面に保存されているスタイルの定義から書式設定を継承します。この動作によって、ファイルのサイズが小さくなり、マスター シェイプの数式やスタイルの定義に対する変更を、すべてのインスタンスに反映することが可能になります。</span><span class="sxs-lookup"><span data-stu-id="616d0-p107">Visio inherits formulas whenever possible. Rather than make a local copy of every formula in the instance, an instance inherits formulas from its master on the document stencil and inherits formatting from the style definition stored with the drawing. This behavior results in smaller files, but also allows changes to the master's formulas or the style definition to be propagated to all instances.</span></span>
  
<span data-ttu-id="616d0-132">セル内の黒いテキストは、継承された数式を表します。</span><span class="sxs-lookup"><span data-stu-id="616d0-132">Black text in a cell indicates an inherited formula.</span></span>
  
## <a name="local-formulas"></a><span data-ttu-id="616d0-133">ローカルの数式</span><span class="sxs-lookup"><span data-stu-id="616d0-133">Local formulas</span></span>

<span data-ttu-id="616d0-p108">インスタンスにローカルの数式を記述するということは、セル内の継承された数式が、ユーザーが定義する数式に置き換わるということです。この操作を行うと、マスター シェイプまたはスタイルにあるセルを今後変更しても、このインスタンスは影響を受けません。これは、ローカルの数式を含んだセルに対しては、継承がブロックされるためです。</span><span class="sxs-lookup"><span data-stu-id="616d0-p108">When you write a local formula for an instance, you are replacing the inherited formula in the cell with a local override. Future changes to that cell in the master or style do not affect this instance because it has blocked inheritance for the cell with the local override.</span></span>
  
<span data-ttu-id="616d0-136">関連するセルのローカルの数式は、GUARD 関数を使用して保護しない限り、スタイルを適用するとすべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="616d0-136">Applying a style deletes all local formulas in the related cells unless you use the GUARD function to protect them.</span></span>
  
<span data-ttu-id="616d0-137">青いテキストはローカルの数式を表します。これは [シェイプシート] ウィンドウで数式を編集したか、図形に変更を加えたことにより、セルの数式がリセットされたことを示します。</span><span class="sxs-lookup"><span data-stu-id="616d0-137">Blue text indicates a local formula, either the result of editing the formula in a ShapeSheet window or some change to the shape that caused Visio to reset the formula for that cell.</span></span>
  
## <a name="automatic-updates-to-formulas"></a><span data-ttu-id="616d0-138">数式の自動更新</span><span class="sxs-lookup"><span data-stu-id="616d0-138">Automatic updates to formulas</span></span>

 <span data-ttu-id="616d0-p109">図面で図形を変更した場合、常に特定のセルが自動的に更新されます。これは、場合によっては入力した数式が置き換わる可能性があることを意味しています。たとえば、コーナー ハンドルをドラッグして図形のサイズを変更すると、[PinX]、[PinY]、[Width]、[Height] の各セルで数式がリセットされます。</span><span class="sxs-lookup"><span data-stu-id="616d0-p109">Visio automatically updates certain cells whenever you change a shape in a drawing. This means that under some circumstances formulas you enter can be replaced. For example, if you drag a corner handle to resize a shape, Visio resets formulas in the PinX, PinY, Width, and Height cells.</span></span> 
  
<span data-ttu-id="616d0-142">必要に応じて、GUARD 関数を使用して数式が変更されないように保護できます。</span><span class="sxs-lookup"><span data-stu-id="616d0-142">If necessary, you can protect formulas against changes by using the GUARD function.</span></span>
  

