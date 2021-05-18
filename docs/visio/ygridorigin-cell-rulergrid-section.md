---
title: '[YGridOrigin] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1205
localization_priority: Normal
ms.assetid: eeec59f8-f301-5639-ffd6-8a36b2bf9c8f
description: グリッド原点の垂直方向の座標を指定します。
ms.openlocfilehash: fa8ee15d5ef2b5d581a9532336d3983bed17b1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404492"
---
# <a name="ygridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="8920d-103">[YGridOrigin] セル (Ruler &amp; Grid セクション)</span><span class="sxs-lookup"><span data-stu-id="8920d-103">YGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="8920d-104">グリッド原点の垂直方向の座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="8920d-104">Specifies the vertical origin of the grid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8920d-105">注釈</span><span class="sxs-lookup"><span data-stu-id="8920d-105">Remarks</span></span>

<span data-ttu-id="8920d-106">このセルは、[ルーラーグリッド] ダイアログ ボックスの [垂直グリッド原点] オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;**</span><span class="sxs-lookup"><span data-stu-id="8920d-106">This cell corresponds to the vertical **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="8920d-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridOrigin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8920d-107">To get a reference to the YGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8920d-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="8920d-108">Cell name:</span></span>  <br/> |<span data-ttu-id="8920d-109">YGridOrigin</span><span class="sxs-lookup"><span data-stu-id="8920d-109">YGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="8920d-110">プログラムから、インデックスによって [YGridOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8920d-110">To get a reference to the YGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8920d-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8920d-111">Section index:</span></span>  <br/> |<span data-ttu-id="8920d-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8920d-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8920d-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8920d-113">Row index:</span></span>  <br/> |<span data-ttu-id="8920d-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="8920d-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="8920d-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8920d-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8920d-116">**visYGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="8920d-116">**visYGridOrigin**</span></span> <br/> |
   

