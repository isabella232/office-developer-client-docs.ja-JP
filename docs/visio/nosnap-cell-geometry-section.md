---
title: '[NoSnap] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: 他の図形がパスにスナップされるかどうかを指定します。
ms.openlocfilehash: 111f3773cb1df9033ed5a7b0b146d40ce6b26df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805933"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="443dc-103">[NoSnap] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="443dc-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="443dc-104">他の図形がパスにスナップされるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="443dc-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="443dc-105">**値**</span><span class="sxs-lookup"><span data-stu-id="443dc-105">**Value**</span></span>|<span data-ttu-id="443dc-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="443dc-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="443dc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="443dc-107">TRUE</span></span>  <br/> | <span data-ttu-id="443dc-108">他の図形はこのパスにスナップできません。</span><span class="sxs-lookup"><span data-stu-id="443dc-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="443dc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="443dc-109">FALSE</span></span>  <br/> | <span data-ttu-id="443dc-110">他の図形はこのパスにスナップできます。</span><span class="sxs-lookup"><span data-stu-id="443dc-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="443dc-111">備考</span><span class="sxs-lookup"><span data-stu-id="443dc-111">Remarks</span></span>

<span data-ttu-id="443dc-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [nosnap] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="443dc-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="443dc-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="443dc-113">Cell name:</span></span>  <br/> | <span data-ttu-id="443dc-114">ジオメトリの*i*です。[Nosnap]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="443dc-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="443dc-115">プログラムから、インデックスによって [nosnap] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="443dc-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="443dc-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="443dc-116">Section index:</span></span>  <br/> |<span data-ttu-id="443dc-117">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="443dc-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="443dc-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="443dc-118">Row index:</span></span>  <br/> |<span data-ttu-id="443dc-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="443dc-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="443dc-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="443dc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="443dc-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="443dc-121">**visCompNoSnap**</span></span> <br/> |
   

