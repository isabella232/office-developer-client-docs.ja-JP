---
title: '[SketchLineWeight] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: スケッチ効果の結果として、線の太さに追加された厚みを、0 から 50 のポイントで決定します。 [SketchLineWeight] セルの値が大きほど、図形の線の太さが増します。
ms.openlocfilehash: 0ee71bbaec59f5c79b72314b08478f8028b4e0ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404513"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a><span data-ttu-id="7f732-104">[SketchLineWeight] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="7f732-104">SketchLineWeight Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="7f732-105">スケッチ効果の結果として、線の太さに追加された厚みを、0 から 50 のポイントで決定します。</span><span class="sxs-lookup"><span data-stu-id="7f732-105">Determines the additional thickness added to line weight as the result of a sketch effect, in points from 0 to 50.</span></span> <span data-ttu-id="7f732-106">**[SketchLineWeight]** セルの値が大きほど、図形の線の太さが増します。</span><span class="sxs-lookup"><span data-stu-id="7f732-106">The thickness of a shape's line increases as the value of the **SketchLineWeight** cell increases.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7f732-107">注釈</span><span class="sxs-lookup"><span data-stu-id="7f732-107">Remarks</span></span>

<span data-ttu-id="7f732-108">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchLineWeight**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f732-108">To get a reference to the **SketchLineWeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f732-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="7f732-109">Cell name:</span></span>  <br/> | <span data-ttu-id="7f732-110">SketchLineWeight</span><span class="sxs-lookup"><span data-stu-id="7f732-110">SketchLineWeight</span></span>  <br/> |
   
<span data-ttu-id="7f732-111">プログラムから、インデックスによって [**SketchLineWeight**] セルへの参照を取得するには、**SketchLineWeight** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f732-111">To get a reference to the **SketchLineWeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f732-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7f732-112">Section index:</span></span>  <br/> |<span data-ttu-id="7f732-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7f732-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7f732-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7f732-114">Row index:</span></span>  <br/> |<span data-ttu-id="7f732-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="7f732-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="7f732-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7f732-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7f732-117">**visSketchLineWeight**</span><span class="sxs-lookup"><span data-stu-id="7f732-117">**visSketchLineWeight**</span></span> <br/> |
   

