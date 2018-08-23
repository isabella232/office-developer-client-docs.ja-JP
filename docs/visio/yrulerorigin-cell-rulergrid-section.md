---
title: '[YRulerOrigin] セル ([ルーラーとグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1220
localization_priority: Normal
ms.assetid: 5d21b64f-a559-76ef-06df-d24c048cc6ef
description: ページの y 軸のルーラーに対して、ゼロ点を指定します。
ms.openlocfilehash: 143f372d66ee25e90608a9b2eb252a99e7bcc52f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806850"
---
# <a name="yrulerorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="598d1-103">[YRulerOrigin] セル ([ルーラーとグリッド] セクション)</span><span class="sxs-lookup"><span data-stu-id="598d1-103">YRulerOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="598d1-104">ページの y 軸のルーラーに対して、ゼロ点を指定します。</span><span class="sxs-lookup"><span data-stu-id="598d1-104">Specifies the zero point on the y-axis ruler for the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="598d1-105">注釈</span><span class="sxs-lookup"><span data-stu-id="598d1-105">Remarks</span></span>

<span data-ttu-id="598d1-106">このセル内の垂直方向の**ルーラーのゼロ点**] オプションに対応して、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。</span><span class="sxs-lookup"><span data-stu-id="598d1-106">This cell corresponds to the vertical **Ruler zero** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="598d1-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YRulerOrigin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="598d1-107">To get a reference to the YRulerOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="598d1-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="598d1-108">Cell name:</span></span>  <br/> |<span data-ttu-id="598d1-109">YRulerOrigin</span><span class="sxs-lookup"><span data-stu-id="598d1-109">YRulerOrigin</span></span>  <br/> |
   
<span data-ttu-id="598d1-110">プログラムから、インデックスによって [YRulerOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="598d1-110">To get a reference to the YRulerOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="598d1-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="598d1-111">Section index:</span></span>  <br/> |<span data-ttu-id="598d1-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="598d1-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="598d1-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="598d1-113">Row index:</span></span>  <br/> |<span data-ttu-id="598d1-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="598d1-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="598d1-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="598d1-115">Cell index:</span></span>  <br/> |<span data-ttu-id="598d1-116">**visYRulerOrigin**</span><span class="sxs-lookup"><span data-stu-id="598d1-116">**visYRulerOrigin**</span></span> <br/> |
   

