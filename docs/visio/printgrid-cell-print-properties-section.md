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
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="50b58-103">[PrintGrid] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="50b58-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="50b58-104">図面ページの印刷時にグリッドを印刷するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="50b58-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="50b58-105">**値**</span><span class="sxs-lookup"><span data-stu-id="50b58-105">**Value**</span></span>|<span data-ttu-id="50b58-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="50b58-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50b58-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="50b58-107">TRUE</span></span>  <br/> |<span data-ttu-id="50b58-108">このページの印刷時にグリッドを表示します。</span><span class="sxs-lookup"><span data-stu-id="50b58-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="50b58-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="50b58-109">FALSE</span></span>  <br/> |<span data-ttu-id="50b58-110">このページの印刷時にグリッドを表示しません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="50b58-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50b58-111">注釈</span><span class="sxs-lookup"><span data-stu-id="50b58-111">Remarks</span></span>

<span data-ttu-id="50b58-112">この値は、[**ページ設定**] ダイアログ ボックスの [**印刷設定**] タブで [**目盛線**] チェック ボックスに対応 ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。</span><span class="sxs-lookup"><span data-stu-id="50b58-112">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="50b58-113">以外の色 (印刷用グレー)、印刷されたグリッドは、Microsoft Visio の図面ウィンドウに表示するグリッドと同じです。</span><span class="sxs-lookup"><span data-stu-id="50b58-113">Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="50b58-114">ページごとにグリッドを印刷するかどうかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="50b58-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="50b58-115">ページごとにグリッドのスタイルを定義することも、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)、ページがアクティブな場合。</span><span class="sxs-lookup"><span data-stu-id="50b58-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="50b58-116">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [printgrid] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="50b58-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50b58-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="50b58-117">Cell name:</span></span>  <br/> |<span data-ttu-id="50b58-118">[Printgrid]</span><span class="sxs-lookup"><span data-stu-id="50b58-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="50b58-119">プログラムから、インデックスによって [printgrid] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="50b58-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50b58-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="50b58-120">Section index:</span></span>  <br/> |<span data-ttu-id="50b58-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="50b58-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="50b58-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="50b58-122">Row index:</span></span>  <br/> |<span data-ttu-id="50b58-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="50b58-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="50b58-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="50b58-124">Cell index:</span></span>  <br/> |<span data-ttu-id="50b58-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="50b58-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

