---
title: '[xrulerorigin] セル&amp; ([ルーラ Grid] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
localization_priority: Normal
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: ページの x 軸のルーラーに対して、ゼロ点を指定します。
ms.openlocfilehash: d66fd324718ec46b1209c4726eeb2d27c21db8b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435328"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="91c7b-103">[xrulerorigin] セル&amp; ([ルーラ Grid] セクション)</span><span class="sxs-lookup"><span data-stu-id="91c7b-103">XRulerOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="91c7b-104">ページの x 軸のルーラーに対して、ゼロ点を指定します。</span><span class="sxs-lookup"><span data-stu-id="91c7b-104">Specifies the zero point on the x-axis ruler for the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91c7b-105">注釈</span><span class="sxs-lookup"><span data-stu-id="91c7b-105">Remarks</span></span>

<span data-ttu-id="91c7b-106">このセルは、[**ルーラー &amp;グリッド**] ダイアログボックス ([**表示**] タブの [**表示**] 矢印をクリック) の [水平**ルーラーゼロ**] オプションに対応しています。</span><span class="sxs-lookup"><span data-stu-id="91c7b-106">This cell corresponds to the horizontal **Ruler zero** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="91c7b-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XRulerOrigin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="91c7b-107">To get a reference to the XRulerOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91c7b-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="91c7b-108">Cell name:</span></span>  <br/> |<span data-ttu-id="91c7b-109">[xrulerorigin]</span><span class="sxs-lookup"><span data-stu-id="91c7b-109">XRulerOrigin</span></span>  <br/> |
   
<span data-ttu-id="91c7b-110">プログラムから、インデックスによって [XRulerOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="91c7b-110">To get a reference to the XRulerOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91c7b-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="91c7b-111">Section index:</span></span>  <br/> |<span data-ttu-id="91c7b-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="91c7b-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="91c7b-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="91c7b-113">Row index:</span></span>  <br/> |<span data-ttu-id="91c7b-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="91c7b-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="91c7b-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="91c7b-115">Cell index:</span></span>  <br/> |<span data-ttu-id="91c7b-116">**visXRulerOrigin**</span><span class="sxs-lookup"><span data-stu-id="91c7b-116">**visXRulerOrigin**</span></span> <br/> |
   

