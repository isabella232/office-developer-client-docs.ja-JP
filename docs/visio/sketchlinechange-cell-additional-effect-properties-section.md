---
title: '[SketchLineChange] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: セクションの長さの割合として、スケッチ効果を使用する場合は、図形の線を図形の座標からのランダム化の量を決定します。 SketchLineChange セルの値を 0% に設定すると、図形の線のジオメトリは、図形の座標を一致します。 値が 100% の場合は、図形の線のジオメトリは、図形のジオメトリを従っていません。
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806505"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="9f8a3-105">[SketchLineChange] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="9f8a3-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="9f8a3-106">セクションの長さの割合として、スケッチ効果を使用する場合は、図形の線を図形の座標からのランダム化の量を決定します。</span><span class="sxs-lookup"><span data-stu-id="9f8a3-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="9f8a3-107">**SketchLineChange**セルの値を 0% に設定すると、図形の線のジオメトリは、図形の座標を一致します。</span><span class="sxs-lookup"><span data-stu-id="9f8a3-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="9f8a3-108">値が 100% の場合は、図形の線のジオメトリは、図形のジオメトリを従っていません。</span><span class="sxs-lookup"><span data-stu-id="9f8a3-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9f8a3-109">備考</span><span class="sxs-lookup"><span data-stu-id="9f8a3-109">Remarks</span></span>

<span data-ttu-id="9f8a3-110">最良の結果を得るには、理想的な**SketchLineChange**のセルの値の範囲は 15% と 50% の間では。</span><span class="sxs-lookup"><span data-stu-id="9f8a3-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="9f8a3-111">15% 未満の値はほとんど気になりません。50% より大きい値は、行をあまりランダムでした。</span><span class="sxs-lookup"><span data-stu-id="9f8a3-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="9f8a3-112">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **SketchLineChange** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="9f8a3-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f8a3-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9f8a3-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="9f8a3-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="9f8a3-115">プログラムから、インデックスによって [ **SketchLineChange** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9f8a3-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f8a3-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-116">Section index:</span></span>  <br/> |<span data-ttu-id="9f8a3-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9f8a3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9f8a3-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-118">Row index:</span></span>  <br/> |<span data-ttu-id="9f8a3-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="9f8a3-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="9f8a3-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9f8a3-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="9f8a3-121">**visSketchLineChange**</span></span> <br/> |
   

