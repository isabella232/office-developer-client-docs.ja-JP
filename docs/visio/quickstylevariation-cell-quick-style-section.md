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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433795"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="d1fdc-104">[quickstylevariation] セル (クイックスタイルセクション)</span><span class="sxs-lookup"><span data-stu-id="d1fdc-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="d1fdc-105">図の背景と対照的な色を使用して、テキスト、線、塗りつぶしの色 (またはこれらのプロパティの組み合わせ) の数式と値を上書きするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="d1fdc-106">0、1、2、4、および8のビット単位の値です。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="d1fdc-107">**値**</span><span class="sxs-lookup"><span data-stu-id="d1fdc-107">**Value**</span></span>|<span data-ttu-id="d1fdc-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="d1fdc-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1fdc-109">.0</span><span class="sxs-lookup"><span data-stu-id="d1fdc-109">0</span></span>  <br/> |<span data-ttu-id="d1fdc-110">図形のテキスト、線、または塗りつぶしの色 (またはこれらのプロパティの組み合わせ) は変更しないでください。テーマの背景色に対して表示されたままになります。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="d1fdc-111">1 </span><span class="sxs-lookup"><span data-stu-id="d1fdc-111">1</span></span>  <br/> |<span data-ttu-id="d1fdc-112">図形のテキスト、線、または塗りつぶしの色 (またはこれらのプロパティの組み合わせ) は変更しないでください。テーマの背景色に対して表示されたままになります。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="d1fdc-113">2 </span><span class="sxs-lookup"><span data-stu-id="d1fdc-113">2</span></span>  <br/> |<span data-ttu-id="d1fdc-114">必要に応じて、図形のテキストの色を変更し、テーマの背景色に対して表示されたままにします。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="d1fdc-115">4 </span><span class="sxs-lookup"><span data-stu-id="d1fdc-115">4</span></span>  <br/> |<span data-ttu-id="d1fdc-116">必要に応じて、図形の線の色を変更し、テーマの背景色に対して表示されたままにします。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="d1fdc-117">8 </span><span class="sxs-lookup"><span data-stu-id="d1fdc-117">8</span></span>  <br/> |<span data-ttu-id="d1fdc-118">必要に応じて、図形の塗りつぶしの色を変更して、テーマの背景色に対して表示されたままにします。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1fdc-119">注釈</span><span class="sxs-lookup"><span data-stu-id="d1fdc-119">Remarks</span></span>

<span data-ttu-id="d1fdc-120">[quickstylevariation] セルを使用して、表示されている図形の図形の外側 (たとえば、ネットワーク図にある図形など) の外部にある場合に、テキストまたは行を表示します。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="d1fdc-121">セルの既定値は0です。これは、その動作が非アクティブであることを意味します。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="d1fdc-122">その他の値を指定すると、セルの動作がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="d1fdc-123">[quickstylevariation] の値は、色 (文字セクション)、[fillforegnd]、または linecolor] のいずれかのセルに配置されたときに、その関数によって生成された値よりも優先されます (または、これら3つのプロパティへの直接参照によって生成される)。文字の色 ")、評価 (" FillColor ")、および評価 (" linecolor] "))。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="d1fdc-124">別の数式から、名前によって [ **[quickstylevariation]** ] セルへの参照を取得するには、 **cell**要素の**N**属性の値を取得するか、または**CellsU**プロパティを使用してプログラムから、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1fdc-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="d1fdc-125">Cell name:</span></span>  <br/> |<span data-ttu-id="d1fdc-126">[quickstylevariation]</span><span class="sxs-lookup"><span data-stu-id="d1fdc-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="d1fdc-127">プログラムから、インデックスによって [ **[quickstylevariation]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d1fdc-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1fdc-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1fdc-128">Section index:</span></span>  <br/> |<span data-ttu-id="d1fdc-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d1fdc-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d1fdc-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1fdc-130">Row index:</span></span>  <br/> |<span data-ttu-id="d1fdc-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="d1fdc-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="d1fdc-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1fdc-132">Cell index:</span></span>  <br/> |<span data-ttu-id="d1fdc-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="d1fdc-133">**visQuickStyleVariation**</span></span> <br/> |
   

