---
title: '[SoftEdgesSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: ソフト エッジ効果のサイズを、0.00 から 100.00 までのポイントで決定します。 [SoftEdgesSize] セルの値が 0 の場合、図形にソフト エッジは適用されません。
ms.openlocfilehash: e749fefde8e0358cbf4ab8388a61ad703c7d52ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334539"
---
# <a name="softedgessize-cell-additional-effect-properties-section"></a><span data-ttu-id="f340a-104">[SoftEdgesSize] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="f340a-104">SoftEdgesSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="f340a-105">ソフト エッジ効果のサイズを、0.00 から 100.00 までのポイントで決定します。</span><span class="sxs-lookup"><span data-stu-id="f340a-105">Determines the size of a soft edge effect, in points from 0.00 to 100.00.</span></span> <span data-ttu-id="f340a-106">[**SoftEdgesSize**] セルの値が 0 の場合、図形にソフト エッジは適用されません。</span><span class="sxs-lookup"><span data-stu-id="f340a-106">If the **SoftEdgesSize** cell has a value of 0, the shape does not have soft edges.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f340a-107">解説</span><span class="sxs-lookup"><span data-stu-id="f340a-107">Remarks</span></span>

<span data-ttu-id="f340a-108">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SoftEdgesSize**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f340a-108">To get a reference to the **SoftEdgesSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f340a-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="f340a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="f340a-110">[softedgessize]</span><span class="sxs-lookup"><span data-stu-id="f340a-110">SoftEdgesSize</span></span>  <br/> |
   
<span data-ttu-id="f340a-111">プログラムから、インデックスによって **SoftEdgesSize**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f340a-111">To get a reference to the **SoftEdgesSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f340a-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f340a-112">Section index:</span></span>  <br/> |<span data-ttu-id="f340a-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f340a-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f340a-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f340a-114">Row index:</span></span>  <br/> |<span data-ttu-id="f340a-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="f340a-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="f340a-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f340a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f340a-117">**visSoftEdgesSize**</span><span class="sxs-lookup"><span data-stu-id="f340a-117">**visSoftEdgesSize**</span></span> <br/> |
   

