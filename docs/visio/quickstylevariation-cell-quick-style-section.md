---
title: '[QuickStyleVariation] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: 図の背景と対照的な色を使用して、テキスト、線、塗りつぶしの色 (またはそれらのプロパティの組み合わせ) の数式と値を上書きするかどうかを決定します。 値は、0、1、2、4、および 8 のビット形式の OR です。
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433795"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="83b82-104">[QuickStyleVariation] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="83b82-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="83b82-105">図の背景と対照的な色を使用して、テキスト、線、塗りつぶしの色 (またはそれらのプロパティの組み合わせ) の数式と値を上書きするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="83b82-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="83b82-106">値は、0、1、2、4、および 8 のビット形式の OR です。</span><span class="sxs-lookup"><span data-stu-id="83b82-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="83b82-107">**値**</span><span class="sxs-lookup"><span data-stu-id="83b82-107">**Value**</span></span>|<span data-ttu-id="83b82-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="83b82-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="83b82-109">0</span><span class="sxs-lookup"><span data-stu-id="83b82-109">0</span></span>  <br/> |<span data-ttu-id="83b82-110">図形のテキスト、線、塗りつぶしの色 (またはそれらのプロパティの任意の組み合わせ) を変更して、テーマの特定の背景色に対して表示されたままにしない。</span><span class="sxs-lookup"><span data-stu-id="83b82-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="83b82-111">1</span><span class="sxs-lookup"><span data-stu-id="83b82-111">1</span></span>  <br/> |<span data-ttu-id="83b82-112">図形のテキスト、線、塗りつぶしの色 (またはそれらのプロパティの任意の組み合わせ) を変更して、テーマの特定の背景色に対して表示されたままにしない。</span><span class="sxs-lookup"><span data-stu-id="83b82-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="83b82-113">2</span><span class="sxs-lookup"><span data-stu-id="83b82-113">2</span></span>  <br/> |<span data-ttu-id="83b82-114">必要に応じて、図形のテキストの色を変更して、テーマの指定された背景色に対して表示されたままにします。</span><span class="sxs-lookup"><span data-stu-id="83b82-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="83b82-115">4</span><span class="sxs-lookup"><span data-stu-id="83b82-115">4</span></span>  <br/> |<span data-ttu-id="83b82-116">必要に応じて図形の線の色を変更して、テーマの指定された背景色に対して表示されたままにします。</span><span class="sxs-lookup"><span data-stu-id="83b82-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="83b82-117">8</span><span class="sxs-lookup"><span data-stu-id="83b82-117">8</span></span>  <br/> |<span data-ttu-id="83b82-118">必要に応じて、図形の塗りつぶしの色を変更して、テーマの指定された背景色に対して表示されたままにします。</span><span class="sxs-lookup"><span data-stu-id="83b82-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83b82-119">注釈</span><span class="sxs-lookup"><span data-stu-id="83b82-119">Remarks</span></span>

<span data-ttu-id="83b82-120">[QuickStyleVariation] セルを使用して、表示されている図形ジオメトリの外側にあるテキストまたは線の表示を保証します (たとえば、テキスト ボックスが図形の下部 (ネットワーク ダイアグラムなど) の下にある図形の場合)。</span><span class="sxs-lookup"><span data-stu-id="83b82-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="83b82-121">セルの既定値は 0 で、その動作は非アクティブです。</span><span class="sxs-lookup"><span data-stu-id="83b82-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="83b82-122">その他の値を指定すると、セルの動作がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="83b82-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="83b82-123">QuickStyleVariation 値は、THEMEVAL 関数が Color (Character Section)、FillForegnd、または LineColor セルに存在する場合 (または THEMEVAL("CharacterColor")、THEMEVAL("FillColor"))、THEMEVAL("LineColor") を使用してこれら 3 つのプロパティへの直接参照によって生成される場合に、THEMEVAL 関数によって生成される値を上書きします。</span><span class="sxs-lookup"><span data-stu-id="83b82-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="83b82-124">別の数式から名前によって **[QuickStyleVariation]** セルへの参照を取得するには、Cell 要素の **N** 属性の値を取得するか **、CellsU** プロパティを使用してプログラムから取得します。</span><span class="sxs-lookup"><span data-stu-id="83b82-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83b82-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="83b82-125">Cell name:</span></span>  <br/> |<span data-ttu-id="83b82-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="83b82-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="83b82-127">プログラムからインデックスによって **[QuickStyleVariation]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="83b82-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83b82-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="83b82-128">Section index:</span></span>  <br/> |<span data-ttu-id="83b82-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="83b82-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="83b82-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="83b82-130">Row index:</span></span>  <br/> |<span data-ttu-id="83b82-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="83b82-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="83b82-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="83b82-132">Cell index:</span></span>  <br/> |<span data-ttu-id="83b82-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="83b82-133">**visQuickStyleVariation**</span></span> <br/> |
   

