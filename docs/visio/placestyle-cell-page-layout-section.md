---
title: '[PlaceStyle] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、図形をページ上にどのように配置するかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: b3159b765922d6656d12dd42a377322e4a91fc04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420802"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="3db80-103">[PlaceStyle] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="3db80-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="3db80-104">[**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに、図形をページ上にどのように配置するかを指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] で [**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="3db80-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3db80-105">注釈</span><span class="sxs-lookup"><span data-stu-id="3db80-105">Remarks</span></span>

<span data-ttu-id="3db80-106">このセルの値は、**[レイアウトの構成]** ダイアログ ボックスで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3db80-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="3db80-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PlaceStyle] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3db80-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3db80-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="3db80-108">Cell name:</span></span>  <br/> |<span data-ttu-id="3db80-109">[placestyle]</span><span class="sxs-lookup"><span data-stu-id="3db80-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="3db80-110">プログラムから、インデックスによって [PlaceStyle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3db80-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3db80-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3db80-111">Section index:</span></span>  <br/> |<span data-ttu-id="3db80-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3db80-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3db80-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3db80-113">Row index:</span></span>  <br/> |<span data-ttu-id="3db80-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="3db80-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="3db80-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3db80-115">Cell index:</span></span>  <br/> |<span data-ttu-id="3db80-116">**visPLOPlaceStyle**</span><span class="sxs-lookup"><span data-stu-id="3db80-116">**visPLOPlaceStyle**</span></span> <br/> |
   

