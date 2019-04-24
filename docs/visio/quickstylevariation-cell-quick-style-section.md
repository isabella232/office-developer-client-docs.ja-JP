---
title: '[quickstylevariation] セル (クイックスタイルセクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: 図の背景と対照的な色を使用して、テキスト、線、塗りつぶしの色 (またはこれらのプロパティの組み合わせ) の数式と値を上書きするかどうかを指定します。 0、1、2、4、および8のビット単位の値です。
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360015"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="8e190-104">[quickstylevariation] セル (クイックスタイルセクション)</span><span class="sxs-lookup"><span data-stu-id="8e190-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="8e190-105">図の背景と対照的な色を使用して、テキスト、線、塗りつぶしの色 (またはこれらのプロパティの組み合わせ) の数式と値を上書きするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8e190-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="8e190-106">0、1、2、4、および8のビット単位の値です。</span><span class="sxs-lookup"><span data-stu-id="8e190-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="8e190-107">**値**</span><span class="sxs-lookup"><span data-stu-id="8e190-107">**Value**</span></span>|<span data-ttu-id="8e190-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="8e190-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e190-109">.0</span><span class="sxs-lookup"><span data-stu-id="8e190-109">0</span></span>  <br/> |<span data-ttu-id="8e190-110">図形のテキスト、線、または塗りつぶしの色 (またはこれらのプロパティの組み合わせ) は変更しないでください。テーマの背景色に対して表示されたままになります。</span><span class="sxs-lookup"><span data-stu-id="8e190-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="8e190-111">1-d</span><span class="sxs-lookup"><span data-stu-id="8e190-111">1</span></span>  <br/> |<span data-ttu-id="8e190-112">図形のテキスト、線、または塗りつぶしの色 (またはこれらのプロパティの組み合わせ) は変更しないでください。テーマの背景色に対して表示されたままになります。</span><span class="sxs-lookup"><span data-stu-id="8e190-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="8e190-113">pbm-2</span><span class="sxs-lookup"><span data-stu-id="8e190-113">2</span></span>  <br/> |<span data-ttu-id="8e190-114">必要に応じて、図形のテキストの色を変更し、テーマの背景色に対して表示されたままにします。</span><span class="sxs-lookup"><span data-stu-id="8e190-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="8e190-115">2/4</span><span class="sxs-lookup"><span data-stu-id="8e190-115">4</span></span>  <br/> |<span data-ttu-id="8e190-116">必要に応じて、図形の線の色を変更し、テーマの背景色に対して表示されたままにします。</span><span class="sxs-lookup"><span data-stu-id="8e190-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="8e190-117">~</span><span class="sxs-lookup"><span data-stu-id="8e190-117">8</span></span>  <br/> |<span data-ttu-id="8e190-118">必要に応じて、図形の塗りつぶしの色を変更して、テーマの背景色に対して表示されたままにします。</span><span class="sxs-lookup"><span data-stu-id="8e190-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e190-119">解説</span><span class="sxs-lookup"><span data-stu-id="8e190-119">Remarks</span></span>

<span data-ttu-id="8e190-120">[quickstylevariation] セルを使用して、表示されている図形の図形の外側 (たとえば、ネットワーク図にある図形など) の外部にある場合に、テキストまたは行を表示します。</span><span class="sxs-lookup"><span data-stu-id="8e190-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="8e190-121">セルの既定値は0です。これは、その動作が非アクティブであることを意味します。</span><span class="sxs-lookup"><span data-stu-id="8e190-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="8e190-122">その他の値を指定すると、セルの動作がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="8e190-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="8e190-123">[quickstylevariation] の値は、色 (文字セクション)、[fillforegnd]、または linecolor] のいずれかのセルに配置されたときに、その関数によって生成された値よりも優先されます (または、これら3つのプロパティへの直接参照によって生成される)。文字の色 ")、評価 (" FillColor ")、および評価 (" linecolor] "))。</span><span class="sxs-lookup"><span data-stu-id="8e190-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="8e190-124">別の数式から、名前によって [ **[quickstylevariation]** ] セルへの参照を取得するには、 **cell**要素の**N**属性の値を取得するか、または**CellsU**プロパティを使用してプログラムから、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8e190-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e190-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="8e190-125">Cell name:</span></span>  <br/> |<span data-ttu-id="8e190-126">[quickstylevariation]</span><span class="sxs-lookup"><span data-stu-id="8e190-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="8e190-127">プログラムから、インデックスによって [ **[quickstylevariation]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e190-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e190-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8e190-128">Section index:</span></span>  <br/> |<span data-ttu-id="8e190-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8e190-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8e190-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8e190-130">Row index:</span></span>  <br/> |<span data-ttu-id="8e190-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="8e190-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="8e190-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8e190-132">Cell index:</span></span>  <br/> |<span data-ttu-id="8e190-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="8e190-133">**visQuickStyleVariation**</span></span> <br/> |
   

