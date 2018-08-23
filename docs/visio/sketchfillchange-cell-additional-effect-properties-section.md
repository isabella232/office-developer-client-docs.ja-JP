---
title: '[SketchFillChange] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: セクションの長さの割合として、スケッチ効果を使用する場合は、図形の塗りつぶしを図形の座標からのランダム化の量を決定します。 SketchFillChange セルの値を 0% に設定すると、図形の塗りつぶしの境界のジオメトリは、図形の座標を一致します。 値が 100% の場合は、図形の塗りつぶしの境界のジオメトリは、図形のジオメトリを従っていません。
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806510"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="8ca2e-105">[SketchFillChange] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="8ca2e-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="8ca2e-106">セクションの長さの割合として、スケッチ効果を使用する場合は、図形の塗りつぶしを図形の座標からのランダム化の量を決定します。</span><span class="sxs-lookup"><span data-stu-id="8ca2e-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="8ca2e-107">**SketchFillChange**セルの値を 0% に設定すると、図形の塗りつぶしの境界のジオメトリは、図形の座標を一致します。</span><span class="sxs-lookup"><span data-stu-id="8ca2e-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="8ca2e-108">値が 100% の場合は、図形の塗りつぶしの境界のジオメトリは、図形のジオメトリを従っていません。</span><span class="sxs-lookup"><span data-stu-id="8ca2e-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8ca2e-109">注釈</span><span class="sxs-lookup"><span data-stu-id="8ca2e-109">Remarks</span></span>

<span data-ttu-id="8ca2e-p103">最適な結果を得るための [**SketchFillChange**] セルの値の理想的な範囲は、15% から 50% の間です。15% を下回る値ではほとんどわからず、50% を上回る値ではランダム化がいっそう強くなります。</span><span class="sxs-lookup"><span data-stu-id="8ca2e-p103">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%. A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="8ca2e-112">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchFillChange**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ca2e-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ca2e-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="8ca2e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="8ca2e-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="8ca2e-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="8ca2e-115">プログラムから、インデックスによって [**SketchFillChange**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8ca2e-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ca2e-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8ca2e-116">Section index:</span></span>  <br/> |<span data-ttu-id="8ca2e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8ca2e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8ca2e-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8ca2e-118">Row index:</span></span>  <br/> |<span data-ttu-id="8ca2e-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="8ca2e-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="8ca2e-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8ca2e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8ca2e-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="8ca2e-121">**visSketchFillChange**</span></span> <br/> |
   

