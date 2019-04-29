---
title: '[PrintGrid] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: 図面ページの印刷時にグリッドを印刷するかどうかを指定します。
ms.openlocfilehash: 9b98999cd02fa6a47ec8564bbd7337ecf8637306
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433207"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="c56a7-103">[PrintGrid] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="c56a7-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="c56a7-104">図面ページの印刷時にグリッドを印刷するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c56a7-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="c56a7-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c56a7-105">**Value**</span></span>|<span data-ttu-id="c56a7-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="c56a7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c56a7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c56a7-107">TRUE</span></span>  <br/> |<span data-ttu-id="c56a7-108">このページの印刷時にグリッドを表示します。</span><span class="sxs-lookup"><span data-stu-id="c56a7-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="c56a7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c56a7-109">FALSE</span></span>  <br/> |<span data-ttu-id="c56a7-110">このページの印刷時にグリッドを表示しません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="c56a7-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c56a7-111">注釈</span><span class="sxs-lookup"><span data-stu-id="c56a7-111">Remarks</span></span>

<span data-ttu-id="c56a7-p101">この値は、[**ページ設定**] ダイアログ ボックスの [**プリンターの設定**] タブにある [**目盛線**] チェック ボックスに対応しています (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックします)。印刷されたグリッドは、色 (印刷ではグレー) 以外の点では、Microsoft Visio 図面ウィンドウに表示されるグリッドと同じです。</span><span class="sxs-lookup"><span data-stu-id="c56a7-p101">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="c56a7-114">グリッドを 1 ページずつ印刷するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c56a7-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="c56a7-115">また、グリッドのスタイルは、ページがアクティブなときに [**表示**] タブの [**表示**] をクリックすると表示される [**ルーラー &amp;グリッド**] ダイアログボックスで、ページごとに定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="c56a7-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="c56a7-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PrintGrid] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c56a7-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c56a7-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="c56a7-117">Cell name:</span></span>  <br/> |<span data-ttu-id="c56a7-118">[printgrid]</span><span class="sxs-lookup"><span data-stu-id="c56a7-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="c56a7-119">プログラムから、インデックスによって [PrintGrid] セルへの参照を取得するには、**CellsSRC** プロパティを使用します。次の引数を指定してください。</span><span class="sxs-lookup"><span data-stu-id="c56a7-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c56a7-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c56a7-120">Section index:</span></span>  <br/> |<span data-ttu-id="c56a7-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c56a7-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c56a7-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c56a7-122">Row index:</span></span>  <br/> |<span data-ttu-id="c56a7-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="c56a7-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="c56a7-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c56a7-124">Cell index:</span></span>  <br/> |<span data-ttu-id="c56a7-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="c56a7-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

