---
title: '[PageScale] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: 現在の図面縮尺でページ単位の値を指定します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。
ms.openlocfilehash: 0e1721ea667ad3bcd9f35880ab4e63bc90802c32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806001"
---
# <a name="pagescale-cell-page-properties-section"></a><span data-ttu-id="ae674-104">[PageScale] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="ae674-104">PageScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="ae674-p102">現在の図面縮尺でページ単位の値を指定します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。</span><span class="sxs-lookup"><span data-stu-id="ae674-p102">Determines the value of the page unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae674-107">注釈</span><span class="sxs-lookup"><span data-stu-id="ae674-107">Remarks</span></span>

<span data-ttu-id="ae674-108">**[ページ設定**] ダイアログ ボックスで [**図面縮尺**] タブの [pagescale] セルの値を設定することもできます ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。</span><span class="sxs-lookup"><span data-stu-id="ae674-108">You can also set the value of the PageScale cell on the **Drawing Scale** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="ae674-109">セルの値は、最初の**既定の縮尺**] ボックスまたは **[縮尺**] ボックスの [**図面縮尺**で選択した図面縮尺の設定に応じて、2 つの数値です。</span><span class="sxs-lookup"><span data-stu-id="ae674-109">The value of the cell is the first of the two numbers in the **Pre-defined scale** box or **Custom scale** box, depending on the drawing scale setting selected under **Drawing scale**.</span></span> <span data-ttu-id="ae674-110">などの場合は、図面に建築系縮尺を選択すると、ページの図面縮尺は 3/32"= 1'0"です。</span><span class="sxs-lookup"><span data-stu-id="ae674-110">For example, if you select an architectural scale for your drawing, the drawing scale for the page is 3/32" = 1'0".</span></span> <span data-ttu-id="ae674-111">[Pagescale] セルの値は 0.0938 のです。</span><span class="sxs-lookup"><span data-stu-id="ae674-111">The value in the PageScale cell is 0.0938 in.</span></span> <span data-ttu-id="ae674-112">(または 3/32 インチ) し、[DrawingScale] セルに値が 1 フィートです。</span><span class="sxs-lookup"><span data-stu-id="ae674-112">(or 3/32") and the value in the DrawingScale cell is 1 ft.</span></span>
  
<span data-ttu-id="ae674-113">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [pagescale] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ae674-113">To get a reference to the PageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae674-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="ae674-114">Cell name:</span></span>  <br/> |<span data-ttu-id="ae674-115">[Pagescale]</span><span class="sxs-lookup"><span data-stu-id="ae674-115">PageScale</span></span>  <br/> |
   
<span data-ttu-id="ae674-116">プログラムから、インデックスによって [pagescale] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae674-116">To get a reference to the PageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae674-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae674-117">Section index:</span></span>  <br/> |<span data-ttu-id="ae674-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ae674-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ae674-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae674-119">Row index:</span></span>  <br/> |<span data-ttu-id="ae674-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="ae674-120">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="ae674-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae674-121">Cell index:</span></span>  <br/> |<span data-ttu-id="ae674-122">**visPageScale**</span><span class="sxs-lookup"><span data-stu-id="ae674-122">**visPageScale**</span></span> <br/> |
   

