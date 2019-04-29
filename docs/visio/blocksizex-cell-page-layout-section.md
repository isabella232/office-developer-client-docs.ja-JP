---
title: '[BlockSizeX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: '[レイアウトの構成] ダイアログボックス ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリック) を使用して図形をレイアウトするときに、水平方向のブロックサイズを決定します。'
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424190"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="a67e6-103">[BlockSizeX] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="a67e6-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="a67e6-104">[**レイアウトの構成**] ダイアログボックスを使用して図形をレイアウトするときに、図形の各図形が図面ページ上に配置される領域 ([**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト] をクリックします) を指定します。** をクリックし、[その**他のレイアウトオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="a67e6-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a67e6-105">注釈</span><span class="sxs-lookup"><span data-stu-id="a67e6-105">Remarks</span></span>

<span data-ttu-id="a67e6-106">この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="a67e6-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="a67e6-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BlockSizeX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a67e6-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a67e6-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="a67e6-108">Cell name:</span></span>  <br/> |<span data-ttu-id="a67e6-109">[blocksizex]</span><span class="sxs-lookup"><span data-stu-id="a67e6-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="a67e6-110">プログラムから、インデックスによって [BlockSizeX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a67e6-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a67e6-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a67e6-111">Section index:</span></span>  <br/> |<span data-ttu-id="a67e6-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a67e6-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a67e6-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a67e6-113">Row index:</span></span>  <br/> |<span data-ttu-id="a67e6-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a67e6-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="a67e6-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a67e6-115">Cell index:</span></span>  <br/> |<span data-ttu-id="a67e6-116">**visploblocksizex**</span><span class="sxs-lookup"><span data-stu-id="a67e6-116">**visPLOBlockSizeX**</span></span> <br/> |
   

