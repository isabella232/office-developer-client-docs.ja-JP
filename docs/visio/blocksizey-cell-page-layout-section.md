---
title: '[BlockSizeY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
localization_priority: Normal
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: '[レイアウトの構成] ダイアログ ボックス ([デザイン] タブの [レイアウト] グループで、[Re-Layout ページ] をクリックし、[その他のレイアウト オプション] をクリックして、 [レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、各図形が図面ページに収まる領域である垂直方向のブロック サイズを指定します。'
ms.openlocfilehash: 08f2012bb027267810c21ef253a0073bb42d3a96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427403"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="15edd-103">[BlockSizeY] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="15edd-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="15edd-104">[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、各図形が図面ページに収まる必要がある垂直方向のブロック サイズを指定します ([デザイン]タブの [レイアウト] グループで、[再レイアウトページ] をクリックし、[その他のレイアウト オプション] をクリックします)。  </span><span class="sxs-lookup"><span data-stu-id="15edd-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15edd-105">注釈</span><span class="sxs-lookup"><span data-stu-id="15edd-105">Remarks</span></span>

<span data-ttu-id="15edd-106">この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="15edd-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="15edd-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BlockSizeY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="15edd-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15edd-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="15edd-108">Cell name:</span></span>  <br/> | <span data-ttu-id="15edd-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="15edd-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="15edd-110">プログラムから、インデックスによって [BlockSizeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="15edd-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15edd-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="15edd-111">Section index:</span></span>  <br/> |<span data-ttu-id="15edd-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="15edd-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="15edd-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="15edd-113">Row index:</span></span>  <br/> |<span data-ttu-id="15edd-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="15edd-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="15edd-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="15edd-115">Cell index:</span></span>  <br/> |<span data-ttu-id="15edd-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="15edd-116">**visPLOBlockSizeY**</span></span> <br/> |
   

