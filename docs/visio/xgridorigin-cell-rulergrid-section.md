---
title: '[xgridorigin] セル&amp; ([ルーラ Grid] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
localization_priority: Normal
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: グリッド原点の水平方向の座標を指定します。
ms.openlocfilehash: ee58ea7d950dd7e422f8a60a13bac8aa4ed353a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428621"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="0faa7-103">[xgridorigin] セル&amp; ([ルーラ Grid] セクション)</span><span class="sxs-lookup"><span data-stu-id="0faa7-103">XGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="0faa7-104">グリッド原点の水平方向の座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="0faa7-104">Specifies the horizontal coordinate of the grid origin.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0faa7-105">注釈</span><span class="sxs-lookup"><span data-stu-id="0faa7-105">Remarks</span></span>

<span data-ttu-id="0faa7-106">このセルは、[**ルーラー &amp;グリッド**] ダイアログボックス ([**表示**] タブの [表示] 矢印をクリックすると**表示**されます) の [水平方向の**グリッド線**] オプションに対応しています。</span><span class="sxs-lookup"><span data-stu-id="0faa7-106">This cell corresponds to the horizontal **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow.</span></span> 
  
<span data-ttu-id="0faa7-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XGridOrigin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0faa7-107">To get a reference to the XGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0faa7-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="0faa7-108">Cell name:</span></span>  <br/> |<span data-ttu-id="0faa7-109">[xgridorigin]</span><span class="sxs-lookup"><span data-stu-id="0faa7-109">XGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="0faa7-110">プログラムから、インデックスによって [XGridOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0faa7-110">To get a reference to the XGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0faa7-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0faa7-111">Section index:</span></span>  <br/> |<span data-ttu-id="0faa7-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0faa7-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0faa7-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0faa7-113">Row index:</span></span>  <br/> |<span data-ttu-id="0faa7-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="0faa7-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="0faa7-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0faa7-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0faa7-116">**visXGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="0faa7-116">**visXGridOrigin**</span></span> <br/> |
   

