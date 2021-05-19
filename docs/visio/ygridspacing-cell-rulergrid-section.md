---
title: '[YGridSpacing] セル (Ruler &amp; Grid セクション)'
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417463"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="2f875-103">[YGridSpacing] セル (Ruler &amp; Grid セクション)</span><span class="sxs-lookup"><span data-stu-id="2f875-103">YGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="2f875-104">固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="2f875-104">Specifies the distance between vertical lines in a fixed grid (YGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f875-105">注釈</span><span class="sxs-lookup"><span data-stu-id="2f875-105">Remarks</span></span>

<span data-ttu-id="2f875-106">[ルーラー グリッド **] ダイアログ** ボックスの [垂直方向の最小間隔] オプション **に対応します &amp;**([表示] タブの [表示] 矢印を **クリック** します)。</span><span class="sxs-lookup"><span data-stu-id="2f875-106">Corresponds to the vertical **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="2f875-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridSpacing] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2f875-107">To get a reference to the YGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f875-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="2f875-108">Cell name:</span></span>  <br/> |<span data-ttu-id="2f875-109">YGridSpacing</span><span class="sxs-lookup"><span data-stu-id="2f875-109">YGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="2f875-110">プログラムから、インデックスによって [YGridSpacing] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2f875-110">To get a reference to the YGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f875-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f875-111">Section index:</span></span>  <br/> |<span data-ttu-id="2f875-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2f875-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2f875-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f875-113">Row index:</span></span>  <br/> |<span data-ttu-id="2f875-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="2f875-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="2f875-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f875-115">Cell index:</span></span>  <br/> |<span data-ttu-id="2f875-116">**visYGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="2f875-116">**visYGridSpacing**</span></span> <br/> |
   

