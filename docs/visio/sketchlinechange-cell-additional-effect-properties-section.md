---
title: '[SketchLineChange] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: スケッチ効果を使用する場合の図形のジオメトリからの図形の線のランダム化の量を、セクションの長さに対するパーセンテージで指定します。 [SketchLineChange] セルの値が 0% に設定されている場合、図形の線のジオメトリは図形のジオメトリと一致します。 値が 100% の場合、図形の線のジオメトリは図形のジオメトリに従います。
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419507"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="4645b-105">[SketchLineChange] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="4645b-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="4645b-106">スケッチ効果を使用する場合の図形のジオメトリからの図形の線のランダム化の量を、セクションの長さに対するパーセンテージで指定します。</span><span class="sxs-lookup"><span data-stu-id="4645b-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="4645b-107">**[SketchLineChange]** セルの値が 0% に設定されている場合、図形の線のジオメトリは図形のジオメトリと一致します。</span><span class="sxs-lookup"><span data-stu-id="4645b-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="4645b-108">値が 100% の場合、図形の線のジオメトリは図形のジオメトリに従います。</span><span class="sxs-lookup"><span data-stu-id="4645b-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4645b-109">注釈</span><span class="sxs-lookup"><span data-stu-id="4645b-109">Remarks</span></span>

<span data-ttu-id="4645b-p103">最適な結果を得るための [**SketchLineChange**] セルの値の理想的な範囲は、15% から 50% の間です。15% を下回る値ではほとんどわからず、50% を上回る値では線が過度にランダム化される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4645b-p103">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%. A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="4645b-112">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchLineChange**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4645b-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4645b-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="4645b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4645b-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="4645b-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="4645b-115">プログラムから、インデックスによって [**SketchLineChange**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4645b-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4645b-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4645b-116">Section index:</span></span>  <br/> |<span data-ttu-id="4645b-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4645b-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4645b-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4645b-118">Row index:</span></span>  <br/> |<span data-ttu-id="4645b-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="4645b-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="4645b-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4645b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4645b-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="4645b-121">**visSketchLineChange**</span></span> <br/> |
   

