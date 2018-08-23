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
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805272"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="ebc2d-102">[DropOnPageScale] セル ([その他] セクション)</span><span class="sxs-lookup"><span data-stu-id="ebc2d-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ebc2d-103">図形を図面ページにドロップしたときの縮尺のパーセント値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ebc2d-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebc2d-104">備考</span><span class="sxs-lookup"><span data-stu-id="ebc2d-104">Remarks</span></span>

<span data-ttu-id="ebc2d-105">次の 2 つの場合に Visio は図形を図面ページで適切に表示されるよう縮尺します。</span><span class="sxs-lookup"><span data-stu-id="ebc2d-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="ebc2d-106">縮尺図面に未測定図形をドロップしたとき。</span><span class="sxs-lookup"><span data-stu-id="ebc2d-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="ebc2d-107">非縮尺図面に測定済み図形をドロップしたとき。</span><span class="sxs-lookup"><span data-stu-id="ebc2d-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="ebc2d-108">DropOnPageScale] セルの割合が、縮小される因数を Visio 図形のいずれかの方法を示します (\>100)、下 (\<100)。</span><span class="sxs-lookup"><span data-stu-id="ebc2d-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="ebc2d-109">係数としてこの番号を使用するには、ハード コーディングされた値を計算するときです。</span><span class="sxs-lookup"><span data-stu-id="ebc2d-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="ebc2d-110">縮尺図面の測定済み図形または非縮尺図面の未測定図形では、この値は 100% です。</span><span class="sxs-lookup"><span data-stu-id="ebc2d-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="ebc2d-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DropOnPageScale] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ebc2d-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ebc2d-112">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ebc2d-112">Cell name:</span></span>  <br/> | <span data-ttu-id="ebc2d-113">DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="ebc2d-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="ebc2d-114">プログラムから、インデックスによって [DropOnPageScale] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebc2d-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ebc2d-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ebc2d-115">Section index:</span></span>  <br/> |<span data-ttu-id="ebc2d-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ebc2d-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ebc2d-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ebc2d-117">Row index:</span></span>  <br/> |<span data-ttu-id="ebc2d-118">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="ebc2d-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="ebc2d-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ebc2d-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ebc2d-120">**visObjDropOnPageScale**</span><span class="sxs-lookup"><span data-stu-id="ebc2d-120">**visObjDropOnPageScale**</span></span> <br/> |
   

