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
description: レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトした後で、図面ページを拡大するかどうか ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806230"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="e9cd6-103">[ResizePage] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="e9cd6-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="e9cd6-104">**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトした後で、図面ページを拡大するかどうか ([**デザイン**] タブの [**レイアウト**] で、**再レイアウト**] ページをクリックし、**以上のレイアウト] をクリックし、オプション**)。</span><span class="sxs-lookup"><span data-stu-id="e9cd6-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="e9cd6-105">**値**</span><span class="sxs-lookup"><span data-stu-id="e9cd6-105">**Value**</span></span>|<span data-ttu-id="e9cd6-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="e9cd6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e9cd6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e9cd6-107">TRUE</span></span>  <br/> | <span data-ttu-id="e9cd6-108">ページを拡大します。</span><span class="sxs-lookup"><span data-stu-id="e9cd6-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="e9cd6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e9cd6-109">FALSE</span></span>  <br/> | <span data-ttu-id="e9cd6-110">ページを拡大しません。</span><span class="sxs-lookup"><span data-stu-id="e9cd6-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9cd6-111">注釈</span><span class="sxs-lookup"><span data-stu-id="e9cd6-111">Remarks</span></span>

<span data-ttu-id="e9cd6-112">取得する、[ResizePage] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e9cd6-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9cd6-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="e9cd6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e9cd6-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="e9cd6-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="e9cd6-115">プログラムから、インデックスによって [ResizePage] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e9cd6-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9cd6-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e9cd6-116">Section index:</span></span>  <br/> |<span data-ttu-id="e9cd6-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e9cd6-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e9cd6-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e9cd6-118">Row index:</span></span>  <br/> |<span data-ttu-id="e9cd6-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e9cd6-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="e9cd6-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e9cd6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e9cd6-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="e9cd6-121">**visPLOResizePage**</span></span> <br/> |
   

