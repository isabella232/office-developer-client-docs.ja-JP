---
title: XGridOrigin セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
localization_priority: Normal
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: グリッド原点の水平方向の座標を指定します。
ms.openlocfilehash: 0cc6ff10f9bb4ba7ee0a13a48cb55b7dcd0fa013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806822"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="fcfe3-103">XGridOrigin セル (ルーラー&amp;グリッド セクション)</span><span class="sxs-lookup"><span data-stu-id="fcfe3-103">XGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="fcfe3-104">グリッド原点の水平方向の座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="fcfe3-104">Specifies the horizontal coordinate of the grid origin.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fcfe3-105">注釈</span><span class="sxs-lookup"><span data-stu-id="fcfe3-105">Remarks</span></span>

<span data-ttu-id="fcfe3-106">このセルは水平方向の**グリッドの基準**に対応してオプションで、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示**します。</span><span class="sxs-lookup"><span data-stu-id="fcfe3-106">This cell corresponds to the horizontal **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow.</span></span> 
  
<span data-ttu-id="fcfe3-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[XGridOrigin] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="fcfe3-107">To get a reference to the XGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcfe3-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="fcfe3-108">Cell name:</span></span>  <br/> |<span data-ttu-id="fcfe3-109">XGridOrigin</span><span class="sxs-lookup"><span data-stu-id="fcfe3-109">XGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="fcfe3-110">プログラムから、インデックスによって [XGridOrigin] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="fcfe3-110">To get a reference to the XGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcfe3-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fcfe3-111">Section index:</span></span>  <br/> |<span data-ttu-id="fcfe3-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fcfe3-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fcfe3-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fcfe3-113">Row index:</span></span>  <br/> |<span data-ttu-id="fcfe3-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="fcfe3-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="fcfe3-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fcfe3-115">Cell index:</span></span>  <br/> |<span data-ttu-id="fcfe3-116">**visXGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="fcfe3-116">**visXGridOrigin**</span></span> <br/> |
   

