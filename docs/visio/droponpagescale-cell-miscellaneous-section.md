---
title: '[DropOnPageScale] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423763"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="6a372-102">[DropOnPageScale] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="6a372-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="6a372-103">図形を図面ページにドロップしたときの縮尺のパーセント値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6a372-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a372-104">注釈</span><span class="sxs-lookup"><span data-stu-id="6a372-104">Remarks</span></span>

<span data-ttu-id="6a372-105">次の 2 つの場合に Visio は図形を図面ページで適切に表示されるよう縮尺します。</span><span class="sxs-lookup"><span data-stu-id="6a372-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="6a372-106">縮尺図面に未測定図形をドロップしたとき。</span><span class="sxs-lookup"><span data-stu-id="6a372-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="6a372-107">測定された図形がスケールされていない図面にドロップされる場合。</span><span class="sxs-lookup"><span data-stu-id="6a372-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="6a372-108">[DropOnPageScale] セルのパーセンテージは、図形Visio \> (100) または下 ( 100) のスケールの係数を \< 示します。</span><span class="sxs-lookup"><span data-stu-id="6a372-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="6a372-109">ハードコードされた値を計算する場合に、この数字を係数に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6a372-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="6a372-110">縮尺図面の測定済み図形または非縮尺図面の未測定図形では、この値は 100% です。</span><span class="sxs-lookup"><span data-stu-id="6a372-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="6a372-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DropOnPageScale] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6a372-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a372-112">セル名 :</span><span class="sxs-lookup"><span data-stu-id="6a372-112">Cell name:</span></span>  <br/> | <span data-ttu-id="6a372-113">DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="6a372-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="6a372-114">プログラムから、インデックスによって [DropOnPageScale] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6a372-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a372-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6a372-115">Section index:</span></span>  <br/> |<span data-ttu-id="6a372-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a372-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a372-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6a372-117">Row index:</span></span>  <br/> |<span data-ttu-id="6a372-118">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="6a372-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="6a372-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6a372-119">Cell index:</span></span>  <br/> |<span data-ttu-id="6a372-120">**visObjDropOnPageScale**</span><span class="sxs-lookup"><span data-stu-id="6a372-120">**visObjDropOnPageScale**</span></span> <br/> |
   

