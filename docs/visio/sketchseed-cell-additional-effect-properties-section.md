---
title: '[SketchSeed] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: スケッチ効果の図形座標を決定するために使用されるランダム化の値を、正の整数で表します。 [SketchSeed] セルの値は、スケッチ効果を図形に適用するとき、ランダムで作成されます。
ms.openlocfilehash: 3ec58fbfa183d1a6d7bb6960672658f9a6cca073
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315149"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a><span data-ttu-id="89bf9-104">[SketchSeed] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="89bf9-104">SketchSeed Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="89bf9-105">スケッチ効果の図形座標を決定するために使用されるランダム化の値を、正の整数で表します。</span><span class="sxs-lookup"><span data-stu-id="89bf9-105">Represents a randomization value used to determine the geometry of a sketch effect, as a positive integer.</span></span> <span data-ttu-id="89bf9-106">[**SketchSeed**] セルの値は、スケッチ効果を図形に適用するとき、ランダムで作成されます。</span><span class="sxs-lookup"><span data-stu-id="89bf9-106">The value of the **SketchSeed** cell is randomly created when a sketch effect is applied to the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="89bf9-107">解説</span><span class="sxs-lookup"><span data-stu-id="89bf9-107">Remarks</span></span>

<span data-ttu-id="89bf9-108">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchSeed**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="89bf9-108">To get a reference to the **SketchSeed** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="89bf9-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="89bf9-109">Cell name:</span></span>  <br/> | <span data-ttu-id="89bf9-110">[sketchseed]</span><span class="sxs-lookup"><span data-stu-id="89bf9-110">SketchSeed</span></span>  <br/> |
   
<span data-ttu-id="89bf9-111">プログラムから、インデックスによって [**SketchSeed**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="89bf9-111">To get a reference to the **SketchSeed** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="89bf9-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="89bf9-112">Section index:</span></span>  <br/> |<span data-ttu-id="89bf9-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="89bf9-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="89bf9-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="89bf9-114">Row index:</span></span>  <br/> |<span data-ttu-id="89bf9-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="89bf9-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="89bf9-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="89bf9-116">Cell index:</span></span>  <br/> |<span data-ttu-id="89bf9-117">**visSketchSeed**</span><span class="sxs-lookup"><span data-stu-id="89bf9-117">**visSketchSeed**</span></span> <br/> |
   

