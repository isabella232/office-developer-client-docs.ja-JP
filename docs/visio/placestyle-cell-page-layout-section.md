---
title: '[PlaceStyle] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: 図形の配置方法、ページをレイアウトする図形で、[レイアウトの構成] ダイアログ ボックスを使用するときを決定する ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: 251bee427c732fe782c85c4991df07a1deb2a4dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805999"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="d1f68-103">[PlaceStyle] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="d1f68-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="d1f68-104">図形の配置方法、ページをレイアウトする図形で、[**レイアウトの構成**] ダイアログ ボックスを使用するときを決定する ([**デザイン**] タブの [**レイアウト**] で、**ページの再レイアウト**] をクリックし、**他のレイアウト オプション**をクリックし、)。</span><span class="sxs-lookup"><span data-stu-id="d1f68-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1f68-105">備考</span><span class="sxs-lookup"><span data-stu-id="d1f68-105">Remarks</span></span>

<span data-ttu-id="d1f68-106">**レイアウトの構成**] ダイアログ ボックスで、このセルの値を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1f68-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="d1f68-107">取得する、[PlaceStyle] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d1f68-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1f68-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="d1f68-108">Cell name:</span></span>  <br/> |<span data-ttu-id="d1f68-109">PlaceStyle</span><span class="sxs-lookup"><span data-stu-id="d1f68-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="d1f68-110">プログラムから、インデックスによって [PlaceStyle] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d1f68-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1f68-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1f68-111">Section index:</span></span>  <br/> |<span data-ttu-id="d1f68-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d1f68-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d1f68-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1f68-113">Row index:</span></span>  <br/> |<span data-ttu-id="d1f68-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="d1f68-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="d1f68-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1f68-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d1f68-116">**visPLOPlaceStyle**</span><span class="sxs-lookup"><span data-stu-id="d1f68-116">**visPLOPlaceStyle**</span></span> <br/> |
   

