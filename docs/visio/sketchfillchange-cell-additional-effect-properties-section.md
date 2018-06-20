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
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="7feee-105">[SketchFillChange] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="7feee-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="7feee-106">セクションの長さの割合として、スケッチ効果を使用する場合は、図形の塗りつぶしを図形の座標からのランダム化の量を決定します。</span><span class="sxs-lookup"><span data-stu-id="7feee-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="7feee-107">**SketchFillChange**セルの値を 0% に設定すると、図形の塗りつぶしの境界のジオメトリは、図形の座標を一致します。</span><span class="sxs-lookup"><span data-stu-id="7feee-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="7feee-108">値が 100% の場合は、図形の塗りつぶしの境界のジオメトリは、図形のジオメトリを従っていません。</span><span class="sxs-lookup"><span data-stu-id="7feee-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7feee-109">備考</span><span class="sxs-lookup"><span data-stu-id="7feee-109">Remarks</span></span>

<span data-ttu-id="7feee-110">最良の結果を得るには、理想的な**SketchFillChange**のセルの値の範囲は 15% と 50% の間では。</span><span class="sxs-lookup"><span data-stu-id="7feee-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="7feee-111">15% 未満の値はほとんど気になりません。50% より大きい値はよりランダム化された増加します。</span><span class="sxs-lookup"><span data-stu-id="7feee-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="7feee-112">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **SketchFillChange** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="7feee-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7feee-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="7feee-113">Cell name:</span></span>  <br/> | <span data-ttu-id="7feee-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="7feee-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="7feee-115">プログラムから、インデックスによって [ **SketchFillChange** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7feee-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7feee-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7feee-116">Section index:</span></span>  <br/> |<span data-ttu-id="7feee-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7feee-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7feee-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7feee-118">Row index:</span></span>  <br/> |<span data-ttu-id="7feee-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="7feee-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="7feee-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7feee-120">Cell index:</span></span>  <br/> |<span data-ttu-id="7feee-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="7feee-121">**visSketchFillChange**</span></span> <br/> |
   

