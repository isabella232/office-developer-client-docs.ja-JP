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
description: '[レイアウトの構成] ダイアログ ボックスでレイアウトを構成するときに、表示されない内部的なページ グリッドを基準にして図形をレイアウトするかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424442"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="75ac9-104">[EnableGrid] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="75ac9-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="75ac9-p102">[**レイアウトの構成**] ダイアログ ボックスでレイアウトを構成するときに、表示されない内部的なページ グリッドを基準にして図形をレイアウトするかどうかを指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="75ac9-p102">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box. (On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="75ac9-107">**値**</span><span class="sxs-lookup"><span data-stu-id="75ac9-107">**Value**</span></span>|<span data-ttu-id="75ac9-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="75ac9-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75ac9-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="75ac9-109">TRUE</span></span>  <br/> |<span data-ttu-id="75ac9-110">内部ページ グリッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="75ac9-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="75ac9-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="75ac9-111">FALSE</span></span>  <br/> |<span data-ttu-id="75ac9-112">内部ページ グリッドを使用しません。</span><span class="sxs-lookup"><span data-stu-id="75ac9-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75ac9-113">注釈</span><span class="sxs-lookup"><span data-stu-id="75ac9-113">Remarks</span></span>

<span data-ttu-id="75ac9-p103">このページ グリッドは、[**間隔と図形サイズの設定**] ダイアログ ボックスの [**図形の間隔**] と [**図形の平均サイズ**] の値を使用して作成します (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**]、[**間隔**] の順にクリックします)。</span><span class="sxs-lookup"><span data-stu-id="75ac9-p103">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="75ac9-116">この機能を有効にすると、配置可能な各図形の中心点が、内部ページ グリッドのブロックの中心に合わせて整列します。</span><span class="sxs-lookup"><span data-stu-id="75ac9-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="75ac9-117">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableGrid] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="75ac9-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75ac9-118">セル名 :</span><span class="sxs-lookup"><span data-stu-id="75ac9-118">Cell name:</span></span>  <br/> |<span data-ttu-id="75ac9-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="75ac9-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="75ac9-120">プログラムから、インデックスによって [EnableGrid] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="75ac9-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75ac9-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="75ac9-121">Section index:</span></span>  <br/> |<span data-ttu-id="75ac9-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="75ac9-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="75ac9-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="75ac9-123">Row index:</span></span>  <br/> |<span data-ttu-id="75ac9-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="75ac9-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="75ac9-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="75ac9-125">Cell index:</span></span>  <br/> |<span data-ttu-id="75ac9-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="75ac9-126">**visPLOEnableGrid**</span></span> <br/> |
   

