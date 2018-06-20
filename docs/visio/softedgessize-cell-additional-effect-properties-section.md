---
title: '[SoftEdgesSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: 100.00 0.00 からポイントで、ソフト エッジ効果のサイズを決定します。 SoftEdgesSize セルの値が 0 の場合は、図形にはぼかしはありません。
ms.openlocfilehash: 3b301ae2e8c82867be2a486f2e93c2275fbf3914
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806538"
---
# <a name="softedgessize-cell-additional-effect-properties-section"></a><span data-ttu-id="d0074-104">[SoftEdgesSize] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="d0074-104">SoftEdgesSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="d0074-105">100.00 0.00 からポイントで、ソフト エッジ効果のサイズを決定します。</span><span class="sxs-lookup"><span data-stu-id="d0074-105">Determines the size of a soft edge effect, in points from 0.00 to 100.00.</span></span> <span data-ttu-id="d0074-106">**SoftEdgesSize**セルの値が 0 の場合は、図形にはぼかしはありません。</span><span class="sxs-lookup"><span data-stu-id="d0074-106">If the **SoftEdgesSize** cell has a value of 0, the shape does not have soft edges.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0074-107">備考</span><span class="sxs-lookup"><span data-stu-id="d0074-107">Remarks</span></span>

<span data-ttu-id="d0074-108">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **SoftEdgesSize** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d0074-108">To get a reference to the **SoftEdgesSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0074-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="d0074-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d0074-110">SoftEdgesSize</span><span class="sxs-lookup"><span data-stu-id="d0074-110">SoftEdgesSize</span></span>  <br/> |
   
<span data-ttu-id="d0074-111">プログラムから、インデックスによって [ **SoftEdgesSize** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d0074-111">To get a reference to the **SoftEdgesSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0074-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d0074-112">Section index:</span></span>  <br/> |<span data-ttu-id="d0074-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d0074-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d0074-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d0074-114">Row index:</span></span>  <br/> |<span data-ttu-id="d0074-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="d0074-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="d0074-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d0074-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d0074-117">**visSoftEdgesSize**</span><span class="sxs-lookup"><span data-stu-id="d0074-117">**visSoftEdgesSize**</span></span> <br/> |
   

