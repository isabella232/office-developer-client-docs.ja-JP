---
title: '[xgridspacing] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: 固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。
ms.openlocfilehash: 05b68a9721dbfc9c03402d384d976c42ef05b134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327322"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="0a493-103">[xgridspacing] セル&amp; ([ルーラーグリッド] セクション)</span><span class="sxs-lookup"><span data-stu-id="0a493-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="0a493-104">固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a493-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a493-105">解説</span><span class="sxs-lookup"><span data-stu-id="0a493-105">Remarks</span></span>

<span data-ttu-id="0a493-106">このセルは、[**ルーラー &amp;グリッド**] ダイアログボックス ([**表示**] タブの [**表示**] 矢印をクリックすると表示されます) の [上下の**間隔**] オプションに対応しています。</span><span class="sxs-lookup"><span data-stu-id="0a493-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="0a493-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XGridSpacing] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0a493-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a493-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="0a493-108">Cell name:</span></span>  <br/> |<span data-ttu-id="0a493-109">[xgridspacing]</span><span class="sxs-lookup"><span data-stu-id="0a493-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="0a493-110">プログラムから、インデックスによって [XGridSpacing] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a493-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a493-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0a493-111">Section index:</span></span>  <br/> |<span data-ttu-id="0a493-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0a493-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0a493-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0a493-113">Row index:</span></span>  <br/> |<span data-ttu-id="0a493-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="0a493-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="0a493-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0a493-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0a493-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="0a493-116">**visXGridSpacing**</span></span> <br/> |
   

