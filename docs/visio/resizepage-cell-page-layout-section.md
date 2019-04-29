---
title: '[ResizePage] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトした後で、図面が中心に位置するようにページを拡大するかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438093"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="2797e-103">[ResizePage] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="2797e-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="2797e-104">[**レイアウトの構成**] ダイアログボックスを使用して図形をレイアウトした後に、ページを拡大するかどうかを指定します ([**デザイン**] タブの [**レイアウト**] グループで、[ページの**再レイアウト**] をクリックし、[その他のレイアウト] をクリックします)。 **オプション**)。</span><span class="sxs-lookup"><span data-stu-id="2797e-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="2797e-105">**値**</span><span class="sxs-lookup"><span data-stu-id="2797e-105">**Value**</span></span>|<span data-ttu-id="2797e-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="2797e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2797e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2797e-107">TRUE</span></span>  <br/> | <span data-ttu-id="2797e-108">ページを拡大します。</span><span class="sxs-lookup"><span data-stu-id="2797e-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="2797e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2797e-109">FALSE</span></span>  <br/> | <span data-ttu-id="2797e-110">ページを拡大しません。</span><span class="sxs-lookup"><span data-stu-id="2797e-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2797e-111">注釈</span><span class="sxs-lookup"><span data-stu-id="2797e-111">Remarks</span></span>

<span data-ttu-id="2797e-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ResizePage] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2797e-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2797e-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="2797e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2797e-114">[resizepage]</span><span class="sxs-lookup"><span data-stu-id="2797e-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="2797e-115">プログラムから、インデックスによって [ResizePage] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2797e-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2797e-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2797e-116">Section index:</span></span>  <br/> |<span data-ttu-id="2797e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2797e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2797e-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2797e-118">Row index:</span></span>  <br/> |<span data-ttu-id="2797e-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="2797e-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="2797e-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2797e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2797e-121">**visploresizepage**</span><span class="sxs-lookup"><span data-stu-id="2797e-121">**visPLOResizePage**</span></span> <br/> |
   

