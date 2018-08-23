---
title: '[QuickStyleVariation] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: 数式とテキスト、線、および塗りつぶし色 (またはこれらのプロパティの組み合わせ) の色を使用して値を上書きするかどうかにその図の背景のコントラストを決定します。 値は、0、1、2、4、および 8 のビット単位の OR です。
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806140"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="bfcb3-104">[QuickStyleVariation] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="bfcb3-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="bfcb3-105">数式とテキスト、線、および塗りつぶし色 (またはこれらのプロパティの組み合わせ) の色を使用して値を上書きするかどうかにその図の背景のコントラストを決定します。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="bfcb3-106">値は、0、1、2、4、および 8 のビット単位の OR です。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="bfcb3-107">**値**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-107">**Value**</span></span>|<span data-ttu-id="bfcb3-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfcb3-109">0</span><span class="sxs-lookup"><span data-stu-id="bfcb3-109">0</span></span>  <br/> |<span data-ttu-id="bfcb3-110">図形のテキスト、線、または塗りつぶし色 (またはこれらのプロパティの任意の組み合わせ) テーマの特定の背景色を表示したままにするには変わりません。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="bfcb3-111">1</span><span class="sxs-lookup"><span data-stu-id="bfcb3-111">1</span></span>  <br/> |<span data-ttu-id="bfcb3-112">図形のテキスト、線、または塗りつぶし色 (またはこれらのプロパティの任意の組み合わせ) テーマの特定の背景色を表示したままにするには変わりません。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="bfcb3-113">2</span><span class="sxs-lookup"><span data-stu-id="bfcb3-113">2</span></span>  <br/> |<span data-ttu-id="bfcb3-114">背景色が指定されているテーマのに対して表示されたままにするには、必要に応じて図形のテキストの色を変更します。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="bfcb3-115">4</span><span class="sxs-lookup"><span data-stu-id="bfcb3-115">4</span></span>  <br/> |<span data-ttu-id="bfcb3-116">背景色が指定されているテーマのに対して表示されたままにするには、必要に応じて図形の線の色を変更します。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="bfcb3-117">8</span><span class="sxs-lookup"><span data-stu-id="bfcb3-117">8</span></span>  <br/> |<span data-ttu-id="bfcb3-118">背景色が指定されているテーマのに対して表示されたままにするには、必要な場合は、図形の塗りつぶしの色を変更します。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfcb3-119">注釈</span><span class="sxs-lookup"><span data-stu-id="bfcb3-119">Remarks</span></span>

<span data-ttu-id="bfcb3-120">QuickStyleVariation セルを使用して、(たとえば、ネットワーク図などの図形の下端の下のテキスト ボックスは、図形) で表示されている図形ジオメトリの外側である場合、行またはテキストのいずれかの可視性を保証します。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="bfcb3-121">セルの既定値は、0 であり、その動作がアクティブであることを意味します。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="bfcb3-122">その他の値は、セルの動作をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="bfcb3-123">QuickStyleVariation 値のセルの色 ([Character] セクション)、FillForegnd、または線の色である場合に、THEMEVAL 関数によって生成された値をオーバーライド (または THEMEVAL を使用してこれら 3 つのプロパティへの直接参照によって生成される ("CharacterColor」)、THEMEVAL("FillColor")、および THEMEVAL("LineColor"))。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="bfcb3-124">**CellsU**プロパティを使用して**セル**の要素、またはプログラムから、 **N**属性の値を取得することによって、別の数式の名前によって**QuickStyleVariation** ] セルへの参照を取得して、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfcb3-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="bfcb3-125">Cell name:</span></span>  <br/> |<span data-ttu-id="bfcb3-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="bfcb3-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="bfcb3-127">プログラムから、インデックスによって [ **QuickStyleVariation** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="bfcb3-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfcb3-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bfcb3-128">Section index:</span></span>  <br/> |<span data-ttu-id="bfcb3-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bfcb3-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bfcb3-130">Row index:</span></span>  <br/> |<span data-ttu-id="bfcb3-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="bfcb3-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bfcb3-132">Cell index:</span></span>  <br/> |<span data-ttu-id="bfcb3-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-133">**visQuickStyleVariation**</span></span> <br/> |
   

