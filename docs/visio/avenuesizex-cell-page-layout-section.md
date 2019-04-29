---
title: '[AvenueSizeX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: '[レイアウトの構成] ダイアログボックスを使用して図形をレイアウトするときの、図面ページ上の図形の水平方向の間隔を指定します ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリックします)。'
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411646"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="cb9b9-103">[AvenueSizeX] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="cb9b9-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="cb9b9-104">[**レイアウトの構成**] ダイアログボックスを使用して図形をレイアウトするときの、図面ページ上の図形の水平方向の間隔を指定します ([**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックし、[\* \* More] をクリックします)。レイアウトオプション \* \*)。</span><span class="sxs-lookup"><span data-stu-id="cb9b9-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click \*\* More Layout Options \*\*).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb9b9-105">注釈</span><span class="sxs-lookup"><span data-stu-id="cb9b9-105">Remarks</span></span>

<span data-ttu-id="cb9b9-106">この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブで [**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="cb9b9-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="cb9b9-p101">ダイナミック グリッドでは、左右間隔の計算対象となる図形が 1 つだけある場合に [AvenueSizeX] セルの設定が使用されます。ダイナミック グリッドを使用するには、[**表示**] タブの [**視覚的補助**] グループで、[**ダイナミック グリッド**] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="cb9b9-p101">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="cb9b9-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AvenueSizeX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cb9b9-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb9b9-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="cb9b9-110">Cell name:</span></span>  <br/> | <span data-ttu-id="cb9b9-111">[avenuesizey]</span><span class="sxs-lookup"><span data-stu-id="cb9b9-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="cb9b9-112">プログラムから、インデックスによって [AvenueSizeX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb9b9-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb9b9-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cb9b9-113">Section index:</span></span>  <br/> |<span data-ttu-id="cb9b9-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cb9b9-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cb9b9-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cb9b9-115">Row index:</span></span>  <br/> |<span data-ttu-id="cb9b9-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="cb9b9-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="cb9b9-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cb9b9-117">Cell index:</span></span>  <br/> |<span data-ttu-id="cb9b9-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="cb9b9-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

