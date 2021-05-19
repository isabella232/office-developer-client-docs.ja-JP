---
title: '[SketchEnabled] セルl ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0baef353-41a1-4071-b5b4-ae342086fe34
description: ブール型 (Boolean) として、図形にスケッチ効果を表示するかどうかを指定します。
ms.openlocfilehash: 713b9b5579ca0503157b9810ebf6ec849651c9c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418443"
---
# <a name="sketchenabled-cell-additional-effect-properties-section"></a><span data-ttu-id="e195d-103">[SketchEnabled] セルl ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="e195d-103">SketchEnabled Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="e195d-104">ブール型 (Boolean) として、図形にスケッチ効果を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e195d-104">Determines whether a sketch effect is displayed on the shape or not, as a Boolean.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e195d-105">注釈</span><span class="sxs-lookup"><span data-stu-id="e195d-105">Remarks</span></span>

<span data-ttu-id="e195d-106">別の数式、Cell 要素の **N** 属性の値、**または CellsU** プロパティを使用したプログラムから、名前によって **[SketchEnabled]** セルへの参照を取得するには、次の値を使用します。 </span><span class="sxs-lookup"><span data-stu-id="e195d-106">To get a reference to the **SketchEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e195d-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="e195d-107">Cell name:</span></span>  <br/> | <span data-ttu-id="e195d-108">SketchEnabled</span><span class="sxs-lookup"><span data-stu-id="e195d-108">SketchEnabled</span></span>  <br/> |
   
<span data-ttu-id="e195d-109">プログラムから Index によって **[SketchEnabled]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e195d-109">To get a reference to the **SketchEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e195d-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e195d-110">Section index:</span></span>  <br/> |<span data-ttu-id="e195d-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e195d-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e195d-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e195d-112">Row index:</span></span>  <br/> |<span data-ttu-id="e195d-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="e195d-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="e195d-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e195d-114">Cell index:</span></span>  <br/> |<span data-ttu-id="e195d-115">**visSketchEnabled**</span><span class="sxs-lookup"><span data-stu-id="e195d-115">**visSketchEnabled**</span></span> <br/> |
   

