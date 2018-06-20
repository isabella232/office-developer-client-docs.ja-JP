---
title: XGridSpacing セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: 固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806811"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="75713-103">XGridSpacing セル (ルーラー&amp;グリッド セクション)</span><span class="sxs-lookup"><span data-stu-id="75713-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="75713-104">固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="75713-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75713-105">注釈</span><span class="sxs-lookup"><span data-stu-id="75713-105">Remarks</span></span>

<span data-ttu-id="75713-106">このセルは、水平方向の**最小間隔**に対応するオプションで、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。</span><span class="sxs-lookup"><span data-stu-id="75713-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="75713-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[XGridSpacing] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="75713-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75713-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="75713-108">Cell name:</span></span>  <br/> |<span data-ttu-id="75713-109">XGridSpacing</span><span class="sxs-lookup"><span data-stu-id="75713-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="75713-110">プログラムから、インデックスによって [XGridSpacing] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="75713-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75713-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="75713-111">Section index:</span></span>  <br/> |<span data-ttu-id="75713-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="75713-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="75713-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="75713-113">Row index:</span></span>  <br/> |<span data-ttu-id="75713-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="75713-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="75713-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="75713-115">Cell index:</span></span>  <br/> |<span data-ttu-id="75713-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="75713-116">**visXGridSpacing**</span></span> <br/> |
   

