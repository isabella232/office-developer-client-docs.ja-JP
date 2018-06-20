---
title: XRulerOrigin セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
localization_priority: Normal
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: ページの x 軸のルーラーのゼロ点を指定します。
ms.openlocfilehash: 78fab70c8489ddcdfe450ef9f9fd88b6c5040211
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806823"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="a50d9-103">XRulerOrigin セル (ルーラー&amp;グリッド セクション)</span><span class="sxs-lookup"><span data-stu-id="a50d9-103">XRulerOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="a50d9-104">ページの x 軸のルーラーのゼロ点を指定します。</span><span class="sxs-lookup"><span data-stu-id="a50d9-104">Specifies the zero point on the x-axis ruler for the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a50d9-105">備考</span><span class="sxs-lookup"><span data-stu-id="a50d9-105">Remarks</span></span>

<span data-ttu-id="a50d9-106">このセルは、水平**ルーラーのゼロ点**] オプションに対応して、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。</span><span class="sxs-lookup"><span data-stu-id="a50d9-106">This cell corresponds to the horizontal **Ruler zero** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="a50d9-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[XRulerOrigin] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a50d9-107">To get a reference to the XRulerOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a50d9-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="a50d9-108">Cell name:</span></span>  <br/> |<span data-ttu-id="a50d9-109">XRulerOrigin</span><span class="sxs-lookup"><span data-stu-id="a50d9-109">XRulerOrigin</span></span>  <br/> |
   
<span data-ttu-id="a50d9-110">プログラムから、インデックスによって [XRulerOrigin] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a50d9-110">To get a reference to the XRulerOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a50d9-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a50d9-111">Section index:</span></span>  <br/> |<span data-ttu-id="a50d9-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a50d9-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a50d9-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a50d9-113">Row index:</span></span>  <br/> |<span data-ttu-id="a50d9-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="a50d9-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="a50d9-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a50d9-115">Cell index:</span></span>  <br/> |<span data-ttu-id="a50d9-116">**visXRulerOrigin**</span><span class="sxs-lookup"><span data-stu-id="a50d9-116">**visXRulerOrigin**</span></span> <br/> |
   

