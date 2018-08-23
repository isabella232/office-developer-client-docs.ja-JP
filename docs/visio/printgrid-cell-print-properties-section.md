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
ms.openlocfilehash: 76e5b5b4e82c39cbbffbecc710f05a77dbaa6332
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806125"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="b5e9a-103">[PrintGrid] セル ([印刷のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="b5e9a-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="b5e9a-104">図面ページの印刷時にグリッドを印刷するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b5e9a-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="b5e9a-105">**値**</span><span class="sxs-lookup"><span data-stu-id="b5e9a-105">**Value**</span></span>|<span data-ttu-id="b5e9a-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="b5e9a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5e9a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b5e9a-107">TRUE</span></span>  <br/> |<span data-ttu-id="b5e9a-108">このページの印刷時にグリッドを表示します。</span><span class="sxs-lookup"><span data-stu-id="b5e9a-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="b5e9a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b5e9a-109">FALSE</span></span>  <br/> |<span data-ttu-id="b5e9a-110">このページの印刷時にグリッドを表示しません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="b5e9a-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5e9a-111">注釈</span><span class="sxs-lookup"><span data-stu-id="b5e9a-111">Remarks</span></span>

<span data-ttu-id="b5e9a-p101">この値は、[**ページ設定**] ダイアログ ボックスの [**プリンターの設定**] タブにある [**目盛線**] チェック ボックスに対応しています (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックします)。印刷されたグリッドは、色 (印刷ではグレー) 以外の点では、Microsoft Visio 図面ウィンドウに表示されるグリッドと同じです。</span><span class="sxs-lookup"><span data-stu-id="b5e9a-p101">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="b5e9a-114">ページごとにグリッドを印刷するかどうかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="b5e9a-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="b5e9a-115">ページごとにグリッドのスタイルを定義することも、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)、ページがアクティブな場合。</span><span class="sxs-lookup"><span data-stu-id="b5e9a-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="b5e9a-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PrintGrid] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b5e9a-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5e9a-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="b5e9a-117">Cell name:</span></span>  <br/> |<span data-ttu-id="b5e9a-118">[Printgrid]</span><span class="sxs-lookup"><span data-stu-id="b5e9a-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="b5e9a-119">プログラムから、インデックスによって [PrintGrid] セルへの参照を取得するには、**CellsSRC** プロパティを使用します。次の引数を指定してください。</span><span class="sxs-lookup"><span data-stu-id="b5e9a-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5e9a-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b5e9a-120">Section index:</span></span>  <br/> |<span data-ttu-id="b5e9a-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b5e9a-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b5e9a-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b5e9a-122">Row index:</span></span>  <br/> |<span data-ttu-id="b5e9a-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="b5e9a-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="b5e9a-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b5e9a-124">Cell index:</span></span>  <br/> |<span data-ttu-id="b5e9a-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="b5e9a-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

