---
title: '[SketchLineWeight] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: 0 から 50 までのポイントで、スケッチ効果の結果として、線の太さに追加されたその他の太さを決定します。 セルが増加する SketchLineWeight の値として図形の線の太さが大きくなります。
ms.openlocfilehash: 9ab99faab907ddf0d944abbeea39672906b4c03d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806522"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a><span data-ttu-id="28ab3-104">[SketchLineWeight] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="28ab3-104">SketchLineWeight Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="28ab3-105">0 から 50 までのポイントで、スケッチ効果の結果として、線の太さに追加されたその他の太さを決定します。</span><span class="sxs-lookup"><span data-stu-id="28ab3-105">Determines the additional thickness added to line weight as the result of a sketch effect, in points from 0 to 50.</span></span> <span data-ttu-id="28ab3-106">**SketchLineWeight**のセルが値として図形の線の太さが大きくなります。</span><span class="sxs-lookup"><span data-stu-id="28ab3-106">The thickness of a shape's line increases as the value of the **SketchLineWeight** cell increases.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="28ab3-107">備考</span><span class="sxs-lookup"><span data-stu-id="28ab3-107">Remarks</span></span>

<span data-ttu-id="28ab3-108">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **SketchLineWeight** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="28ab3-108">To get a reference to the **SketchLineWeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28ab3-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="28ab3-109">Cell name:</span></span>  <br/> | <span data-ttu-id="28ab3-110">SketchLineWeight</span><span class="sxs-lookup"><span data-stu-id="28ab3-110">SketchLineWeight</span></span>  <br/> |
   
<span data-ttu-id="28ab3-111">プログラムから、インデックスによって [ **SketchLineWeight** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="28ab3-111">To get a reference to the **SketchLineWeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28ab3-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="28ab3-112">Section index:</span></span>  <br/> |<span data-ttu-id="28ab3-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="28ab3-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="28ab3-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="28ab3-114">Row index:</span></span>  <br/> |<span data-ttu-id="28ab3-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="28ab3-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="28ab3-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="28ab3-116">Cell index:</span></span>  <br/> |<span data-ttu-id="28ab3-117">**visSketchLineWeight**</span><span class="sxs-lookup"><span data-stu-id="28ab3-117">**visSketchLineWeight**</span></span> <br/> |
   

