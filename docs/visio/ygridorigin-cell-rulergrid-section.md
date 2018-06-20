---
title: YGridOrigin セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1205
localization_priority: Normal
ms.assetid: eeec59f8-f301-5639-ffd6-8a36b2bf9c8f
description: グリッド原点の垂直方向の座標を指定します。
ms.openlocfilehash: 2d914fc15df8a100066ad17a2e35001fe8a4d587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806840"
---
# <a name="ygridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="a0697-103">YGridOrigin セル (ルーラー&amp;グリッド セクション)</span><span class="sxs-lookup"><span data-stu-id="a0697-103">YGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="a0697-104">グリッド原点の垂直方向の座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0697-104">Specifies the vertical origin of the grid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0697-105">注釈</span><span class="sxs-lookup"><span data-stu-id="a0697-105">Remarks</span></span>

<span data-ttu-id="a0697-106">このセルが垂直方向の**グリッドの基準**に対応してオプションで、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。</span><span class="sxs-lookup"><span data-stu-id="a0697-106">This cell corresponds to the vertical **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="a0697-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[YGridOrigin] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a0697-107">To get a reference to the YGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0697-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="a0697-108">Cell name:</span></span>  <br/> |<span data-ttu-id="a0697-109">YGridOrigin</span><span class="sxs-lookup"><span data-stu-id="a0697-109">YGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="a0697-110">プログラムから、インデックスによって [YGridOrigin] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0697-110">To get a reference to the YGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0697-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0697-111">Section index:</span></span>  <br/> |<span data-ttu-id="a0697-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0697-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a0697-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0697-113">Row index:</span></span>  <br/> |<span data-ttu-id="a0697-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="a0697-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="a0697-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0697-115">Cell index:</span></span>  <br/> |<span data-ttu-id="a0697-116">**visYGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="a0697-116">**visYGridOrigin**</span></span> <br/> |
   

