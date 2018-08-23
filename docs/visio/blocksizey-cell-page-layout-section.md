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
description: 図形の領域は、レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに図面ページに収まる必要があります、垂直方向のブロック サイズを指定 ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: 283723bf902c07cfb044ab73107491df3c170a4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804913"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="db114-103">[BlockSizeY] セル ([ページ レイアウト] セクション)</span><span class="sxs-lookup"><span data-stu-id="db114-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="db114-104">図形の領域は、**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに図面ページに収まる必要があります、垂直方向のブロック サイズを指定 ([**デザイン**] タブの [**レイアウト**] をクリックして **[再レイアウト] ページ**で、および**他のレイアウト オプション**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="db114-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db114-105">注釈</span><span class="sxs-lookup"><span data-stu-id="db114-105">Remarks</span></span>

<span data-ttu-id="db114-106">この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="db114-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="db114-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BlockSizeY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="db114-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db114-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="db114-108">Cell name:</span></span>  <br/> | <span data-ttu-id="db114-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="db114-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="db114-110">プログラムから、インデックスによって [BlockSizeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="db114-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db114-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="db114-111">Section index:</span></span>  <br/> |<span data-ttu-id="db114-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="db114-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="db114-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="db114-113">Row index:</span></span>  <br/> |<span data-ttu-id="db114-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="db114-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="db114-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="db114-115">Cell index:</span></span>  <br/> |<span data-ttu-id="db114-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="db114-116">**visPLOBlockSizeY**</span></span> <br/> |
   

