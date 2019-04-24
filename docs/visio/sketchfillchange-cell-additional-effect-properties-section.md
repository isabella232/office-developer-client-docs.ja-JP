---
title: '[SketchFillChange] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: スケッチ効果を使用するときに、図形の座標からの図形の塗りつぶしのランダム度を指定します。この値は、セクションの長さに対する割合として設定されます。 [sketchfillchange] セルの値が 0% に設定されている場合、図形の塗りつぶしの境界図形は図形の座標に一致します。 値が 100% の場合、図形の塗りつぶしの境界ジオメトリは図形のジオメトリに沿っていません。
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339814"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="b13c1-105">[SketchFillChange] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="b13c1-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="b13c1-106">スケッチ効果を使用するときに、図形の座標からの図形の塗りつぶしのランダム度を指定します。この値は、セクションの長さに対する割合として設定されます。</span><span class="sxs-lookup"><span data-stu-id="b13c1-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="b13c1-107">**[sketchfillchange]** セルの値が 0% に設定されている場合、図形の塗りつぶしの境界図形は図形の座標に一致します。</span><span class="sxs-lookup"><span data-stu-id="b13c1-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="b13c1-108">値が 100% の場合、図形の塗りつぶしの境界ジオメトリは図形のジオメトリに沿っていません。</span><span class="sxs-lookup"><span data-stu-id="b13c1-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b13c1-109">解説</span><span class="sxs-lookup"><span data-stu-id="b13c1-109">Remarks</span></span>

<span data-ttu-id="b13c1-110">最適な結果を得るための [**SketchFillChange**] セルの値の理想的な範囲は、15% から 50% の間です。</span><span class="sxs-lookup"><span data-stu-id="b13c1-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="b13c1-111">15% を下回る値ではほとんどわからず、50% を上回る値ではランダム化がいっそう強くなります。</span><span class="sxs-lookup"><span data-stu-id="b13c1-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="b13c1-112">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchFillChange**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b13c1-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b13c1-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="b13c1-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b13c1-114">[sketchfillchange]</span><span class="sxs-lookup"><span data-stu-id="b13c1-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="b13c1-115">プログラムから、インデックスによって [**SketchFillChange**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b13c1-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b13c1-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b13c1-116">Section index:</span></span>  <br/> |<span data-ttu-id="b13c1-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b13c1-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b13c1-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b13c1-118">Row index:</span></span>  <br/> |<span data-ttu-id="b13c1-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="b13c1-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="b13c1-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b13c1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b13c1-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="b13c1-121">**visSketchFillChange**</span></span> <br/> |
   

