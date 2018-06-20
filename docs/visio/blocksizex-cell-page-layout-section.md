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
description: 図形の領域は、レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに図面ページに収まる必要があります、水平方向のブロック サイズを指定 ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: 68ed13b85583326c25635049d7e85babe62d5eb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804909"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="c0226-103">[BlockSizeX] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="c0226-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="c0226-104">図形の領域は、**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに図面ページに収まる必要があります、水平方向のブロック サイズを指定 ([**デザイン**] タブの [**レイアウト**] をクリックして**再レイアウトのページ**、**他のレイアウト オプション**をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="c0226-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0226-105">備考</span><span class="sxs-lookup"><span data-stu-id="c0226-105">Remarks</span></span>

<span data-ttu-id="c0226-106">**レイアウトと間隔**] ダイアログ ボックスでこの値を設定することもできます ([**デザイン**] タブで、[**ページ設定**] で矢印をクリックして、**レイアウトと経路**] タブをクリックし、[**間隔**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="c0226-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="c0226-107">取得する、[BlockSizeX] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="c0226-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0226-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="c0226-108">Cell name:</span></span>  <br/> |<span data-ttu-id="c0226-109">BlockSizeX</span><span class="sxs-lookup"><span data-stu-id="c0226-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="c0226-110">プログラムから、インデックスによって [BlockSizeX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c0226-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0226-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c0226-111">Section index:</span></span>  <br/> |<span data-ttu-id="c0226-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0226-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c0226-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c0226-113">Row index:</span></span>  <br/> |<span data-ttu-id="c0226-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="c0226-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="c0226-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c0226-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c0226-116">**visPLOBlockSizeX**</span><span class="sxs-lookup"><span data-stu-id="c0226-116">**visPLOBlockSizeX**</span></span> <br/> |
   

