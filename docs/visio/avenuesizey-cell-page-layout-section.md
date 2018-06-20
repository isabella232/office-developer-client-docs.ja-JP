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
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="ddda3-103">[AvenueSizeY] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="ddda3-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="ddda3-104">**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の垂直方向のスペースの量を決定する ([**デザイン**] タブの [**レイアウト**] で、ページの**再レイアウト**] をクリックし、**よりレイアウト オプション**)。</span><span class="sxs-lookup"><span data-stu-id="ddda3-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ddda3-105">備考</span><span class="sxs-lookup"><span data-stu-id="ddda3-105">Remarks</span></span>

<span data-ttu-id="ddda3-106">**レイアウトと間隔**] ダイアログ ボックスでこの値を設定することもできます ([**デザイン**] タブで、[**ページ設定**] で矢印をクリックして、**レイアウトと経路**] タブをクリックし、[**間隔**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="ddda3-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="ddda3-107">ダイナミック グリッドでは、のみ 1 つの図形は垂直方向の間隔を計算するために利用可能な場合に [avenuesizey] セルで設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="ddda3-107">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing.</span></span> <span data-ttu-id="ddda3-108">[**表示**] タブの [**視覚補助**] では、ダイナミック グリッドを使用するには、**ダイナミック グリッド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddda3-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="ddda3-109">取得する [avenuesizey] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ddda3-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddda3-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="ddda3-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ddda3-111">[Avenuesizey]</span><span class="sxs-lookup"><span data-stu-id="ddda3-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="ddda3-112">プログラムから、インデックスによって [avenuesizey] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ddda3-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddda3-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ddda3-113">Section index:</span></span>  <br/> |<span data-ttu-id="ddda3-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ddda3-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ddda3-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ddda3-115">Row index:</span></span>  <br/> |<span data-ttu-id="ddda3-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="ddda3-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="ddda3-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ddda3-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ddda3-118">**visPLOAvenueSizeY**</span><span class="sxs-lookup"><span data-stu-id="ddda3-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

