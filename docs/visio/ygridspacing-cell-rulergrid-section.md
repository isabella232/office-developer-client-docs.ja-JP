---
title: '[ygridspacing] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1210
localization_priority: Normal
ms.assetid: 30766e13-c90d-62fc-9c98-35ad7b0b4056
description: 固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。
ms.openlocfilehash: fc355b4e509494e9e7570122a8a3a7a3ce2e0588
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283430"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="5b17a-103">[ygridspacing] セル&amp; ([ルーラーグリッド] セクション)</span><span class="sxs-lookup"><span data-stu-id="5b17a-103">YGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="5b17a-104">固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b17a-104">Specifies the distance between vertical lines in a fixed grid (YGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b17a-105">解説</span><span class="sxs-lookup"><span data-stu-id="5b17a-105">Remarks</span></span>

<span data-ttu-id="5b17a-106">[**ルーラー &amp;グリッド**] ダイアログボックスの [上下の**最小間隔**] オプションに対応します ([**表示**] タブで [**表示**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="5b17a-106">Corresponds to the vertical **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="5b17a-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridSpacing] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5b17a-107">To get a reference to the YGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b17a-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="5b17a-108">Cell name:</span></span>  <br/> |<span data-ttu-id="5b17a-109">[ygridspacing]</span><span class="sxs-lookup"><span data-stu-id="5b17a-109">YGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="5b17a-110">プログラムから、インデックスによって [YGridSpacing] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b17a-110">To get a reference to the YGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b17a-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5b17a-111">Section index:</span></span>  <br/> |<span data-ttu-id="5b17a-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5b17a-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5b17a-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5b17a-113">Row index:</span></span>  <br/> |<span data-ttu-id="5b17a-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="5b17a-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="5b17a-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5b17a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="5b17a-116">**visygridspacing**</span><span class="sxs-lookup"><span data-stu-id="5b17a-116">**visYGridSpacing**</span></span> <br/> |
   

