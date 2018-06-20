---
title: '[EnableGrid] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: 非表示、内部ページ グリッド ベースのレイアウトの構成] ダイアログ ボックスでレイアウトを構成するときの図形をレイアウトするかどうかを決定します。 ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックして、他のレイアウト オプション] をクリックして)
ms.openlocfilehash: 3371767343132219ebc38134b93afd1da46c7a45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805305"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="8b4ac-104">[EnableGrid] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="8b4ac-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="8b4ac-105">非表示、内部ページ グリッド ベースの**レイアウトの構成**] ダイアログ ボックスでレイアウトを構成するときの図形をレイアウトするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8b4ac-105">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box.</span></span> <span data-ttu-id="8b4ac-106">([**デザイン**] タブの [**レイアウト**] で、**ページの再レイアウト**] をクリックして、**他のレイアウト オプション**] をクリックして)</span><span class="sxs-lookup"><span data-stu-id="8b4ac-106">(On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="8b4ac-107">**値**</span><span class="sxs-lookup"><span data-stu-id="8b4ac-107">**Value**</span></span>|<span data-ttu-id="8b4ac-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="8b4ac-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b4ac-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="8b4ac-109">TRUE</span></span>  <br/> |<span data-ttu-id="8b4ac-110">内部ページ グリッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8b4ac-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="8b4ac-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="8b4ac-111">FALSE</span></span>  <br/> |<span data-ttu-id="8b4ac-112">内部ページ グリッドを使用しません。</span><span class="sxs-lookup"><span data-stu-id="8b4ac-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b4ac-113">注釈</span><span class="sxs-lookup"><span data-stu-id="8b4ac-113">Remarks</span></span>

<span data-ttu-id="8b4ac-114">このページのグリッドを作成するには、**図形間の間隔**は、**図形の平均サイズ**の値を使用して**レイアウトと間隔**] ダイアログ ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="8b4ac-114">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="8b4ac-115">([**デザイン**] タブで、**ページ設定**の矢印をクリックして、[**レイアウトと経路**、および、[**間隔**] をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="8b4ac-115">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="8b4ac-116">この機能を有効にすると、配置可能な各図形の中心点が、内部ページ グリッドのブロックの中心に合わせて整列します。</span><span class="sxs-lookup"><span data-stu-id="8b4ac-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="8b4ac-117">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[EnableGrid] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="8b4ac-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b4ac-118">セル名 :</span><span class="sxs-lookup"><span data-stu-id="8b4ac-118">Cell name:</span></span>  <br/> |<span data-ttu-id="8b4ac-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="8b4ac-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="8b4ac-120">プログラムから、インデックスによって [EnableGrid] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8b4ac-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b4ac-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8b4ac-121">Section index:</span></span>  <br/> |<span data-ttu-id="8b4ac-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8b4ac-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8b4ac-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8b4ac-123">Row index:</span></span>  <br/> |<span data-ttu-id="8b4ac-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8b4ac-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="8b4ac-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8b4ac-125">Cell index:</span></span>  <br/> |<span data-ttu-id="8b4ac-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="8b4ac-126">**visPLOEnableGrid**</span></span> <br/> |
   

