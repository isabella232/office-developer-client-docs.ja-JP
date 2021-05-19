---
title: '[YRulerOrigin] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1220
localization_priority: Normal
ms.assetid: 5d21b64f-a559-76ef-06df-d24c048cc6ef
description: ページの y 軸のルーラーに対して、ゼロ点を指定します。
ms.openlocfilehash: ead9ca453bfeb86f32a943950b297b9b629de95d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420417"
---
# <a name="yrulerorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="74bbb-103">[YRulerOrigin] セル (Ruler &amp; Grid セクション)</span><span class="sxs-lookup"><span data-stu-id="74bbb-103">YRulerOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="74bbb-104">ページの y 軸のルーラーに対して、ゼロ点を指定します。</span><span class="sxs-lookup"><span data-stu-id="74bbb-104">Specifies the zero point on the y-axis ruler for the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="74bbb-105">注釈</span><span class="sxs-lookup"><span data-stu-id="74bbb-105">Remarks</span></span>

<span data-ttu-id="74bbb-106">このセルは、[ルーラー グリッド] ダイアログ ボックスの垂直ルーラー **0** オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;** </span><span class="sxs-lookup"><span data-stu-id="74bbb-106">This cell corresponds to the vertical **Ruler zero** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="74bbb-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YRulerOrigin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="74bbb-107">To get a reference to the YRulerOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74bbb-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="74bbb-108">Cell name:</span></span>  <br/> |<span data-ttu-id="74bbb-109">YRulerOrigin</span><span class="sxs-lookup"><span data-stu-id="74bbb-109">YRulerOrigin</span></span>  <br/> |
   
<span data-ttu-id="74bbb-110">プログラムから、インデックスによって [YRulerOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="74bbb-110">To get a reference to the YRulerOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74bbb-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="74bbb-111">Section index:</span></span>  <br/> |<span data-ttu-id="74bbb-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="74bbb-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="74bbb-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="74bbb-113">Row index:</span></span>  <br/> |<span data-ttu-id="74bbb-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="74bbb-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="74bbb-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="74bbb-115">Cell index:</span></span>  <br/> |<span data-ttu-id="74bbb-116">**visYRulerOrigin**</span><span class="sxs-lookup"><span data-stu-id="74bbb-116">**visYRulerOrigin**</span></span> <br/> |
   

