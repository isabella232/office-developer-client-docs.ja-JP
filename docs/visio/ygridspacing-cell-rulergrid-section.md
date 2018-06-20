---
title: YGridSpacing セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1210
localization_priority: Normal
ms.assetid: 30766e13-c90d-62fc-9c98-35ad7b0b4056
description: 固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。
ms.openlocfilehash: 638479719ee0649bf271403249e2cde2ddccf09c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806848"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="d31a4-103">YGridSpacing セル (ルーラー&amp;グリッド セクション)</span><span class="sxs-lookup"><span data-stu-id="d31a4-103">YGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="d31a4-104">固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="d31a4-104">Specifies the distance between vertical lines in a fixed grid (YGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d31a4-105">注釈</span><span class="sxs-lookup"><span data-stu-id="d31a4-105">Remarks</span></span>

<span data-ttu-id="d31a4-106">垂直方向の**最小間隔**に対応するオプションで、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。</span><span class="sxs-lookup"><span data-stu-id="d31a4-106">Corresponds to the vertical **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="d31a4-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[YGridSpacing] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d31a4-107">To get a reference to the YGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d31a4-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="d31a4-108">Cell name:</span></span>  <br/> |<span data-ttu-id="d31a4-109">YGridSpacing</span><span class="sxs-lookup"><span data-stu-id="d31a4-109">YGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="d31a4-110">プログラムから、インデックスによって [YGridSpacing] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d31a4-110">To get a reference to the YGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d31a4-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d31a4-111">Section index:</span></span>  <br/> |<span data-ttu-id="d31a4-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d31a4-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d31a4-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d31a4-113">Row index:</span></span>  <br/> |<span data-ttu-id="d31a4-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="d31a4-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="d31a4-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d31a4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d31a4-116">**visYGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="d31a4-116">**visYGridSpacing**</span></span> <br/> |
   

