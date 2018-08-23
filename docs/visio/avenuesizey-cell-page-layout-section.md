---
title: '[AvenueSizeY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の垂直方向のスペースの量を決定する ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: af4089a3b215efaf49b8a45929ca94799fffcba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804799"
---
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="e03a3-103">[AvenueSizeY] セル ([ページ レイアウト] セクション)</span><span class="sxs-lookup"><span data-stu-id="e03a3-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="e03a3-104">**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の垂直方向のスペースの量を決定する ([**デザイン**] タブの [**レイアウト**] で、ページの**再レイアウト**] をクリックし、**よりレイアウト オプション**)。</span><span class="sxs-lookup"><span data-stu-id="e03a3-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e03a3-105">注釈</span><span class="sxs-lookup"><span data-stu-id="e03a3-105">Remarks</span></span>

<span data-ttu-id="e03a3-106">この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="e03a3-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="e03a3-p101">ダイナミック グリッドでは、上下の間隔の計算対象となる図形が 1 つだけある場合に [AvenueSizeY] セルの設定が使用されます。ダイナミック グリッドを使用するには、[**表示**] タブの [**視覚的補助**] グループで、[**ダイナミック グリッド**] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e03a3-p101">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="e03a3-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AvenueSizeY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e03a3-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e03a3-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="e03a3-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e03a3-111">[Avenuesizey]</span><span class="sxs-lookup"><span data-stu-id="e03a3-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="e03a3-112">プログラムから、インデックスによって [AvenueSizeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e03a3-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e03a3-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e03a3-113">Section index:</span></span>  <br/> |<span data-ttu-id="e03a3-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e03a3-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e03a3-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e03a3-115">Row index:</span></span>  <br/> |<span data-ttu-id="e03a3-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e03a3-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="e03a3-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e03a3-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e03a3-118">**visPLOAvenueSizeY**</span><span class="sxs-lookup"><span data-stu-id="e03a3-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

