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
description: '[レイアウトの構成] ダイアログ ボックス ([デザイン] タブの [レイアウト] グループで、[ Re-Layout ページ] をクリックし、[ その他のレイアウト オプション] をクリックして) 図形をレイアウトするときに、図面ページ上の図形間の垂直スペースの量を指定します。'
ms.openlocfilehash: 283de8925e34c470fd1f9e78b8ae58882be8b7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420207"
---
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="21f85-103">[AvenueSizeY] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="21f85-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="21f85-104">[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに図面ページ上の図形間の垂直方向の領域の量を指定します ([デザイン]タブの [レイアウト] グループで、[レイアウトの再レイアウト ページ] をクリックし、[その他のレイアウト オプション] をクリックします)。   </span><span class="sxs-lookup"><span data-stu-id="21f85-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21f85-105">注釈</span><span class="sxs-lookup"><span data-stu-id="21f85-105">Remarks</span></span>

<span data-ttu-id="21f85-106">この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="21f85-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="21f85-p101">ダイナミック グリッドでは、上下の間隔の計算対象となる図形が 1 つだけある場合に [AvenueSizeY] セルの設定が使用されます。ダイナミック グリッドを使用するには、[**表示**] タブの [**視覚的補助**] グループで、[**ダイナミック グリッド**] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="21f85-p101">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="21f85-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AvenueSizeY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="21f85-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="21f85-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="21f85-110">Cell name:</span></span>  <br/> | <span data-ttu-id="21f85-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="21f85-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="21f85-112">プログラムから、インデックスによって [AvenueSizeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="21f85-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="21f85-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="21f85-113">Section index:</span></span>  <br/> |<span data-ttu-id="21f85-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="21f85-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="21f85-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="21f85-115">Row index:</span></span>  <br/> |<span data-ttu-id="21f85-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="21f85-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="21f85-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="21f85-117">Cell index:</span></span>  <br/> |<span data-ttu-id="21f85-118">**visPLOAvenueSizeY**</span><span class="sxs-lookup"><span data-stu-id="21f85-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

