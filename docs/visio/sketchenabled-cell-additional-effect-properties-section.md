---
title: '[SketchEnabled] セルl ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0baef353-41a1-4071-b5b4-ae342086fe34
description: 図形にスケッチ効果を表示するかどうかを、ブール型 (Boolean) の値で指定します。
ms.openlocfilehash: 713b9b5579ca0503157b9810ebf6ec849651c9c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314785"
---
# <a name="sketchenabled-cell-additional-effect-properties-section"></a><span data-ttu-id="efd06-103">[SketchEnabled] セルl ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="efd06-103">SketchEnabled Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="efd06-104">図形にスケッチ効果を表示するかどうかを、ブール型 (Boolean) の値で指定します。</span><span class="sxs-lookup"><span data-stu-id="efd06-104">Determines whether a sketch effect is displayed on the shape or not, as a Boolean.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="efd06-105">解説</span><span class="sxs-lookup"><span data-stu-id="efd06-105">Remarks</span></span>

<span data-ttu-id="efd06-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[sketchenabled]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="efd06-106">To get a reference to the **SketchEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="efd06-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="efd06-107">Cell name:</span></span>  <br/> | <span data-ttu-id="efd06-108">[sketchenabled]</span><span class="sxs-lookup"><span data-stu-id="efd06-108">SketchEnabled</span></span>  <br/> |
   
<span data-ttu-id="efd06-109">プログラムから、インデックスによって [ **[sketchenabled]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="efd06-109">To get a reference to the **SketchEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="efd06-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="efd06-110">Section index:</span></span>  <br/> |<span data-ttu-id="efd06-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="efd06-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="efd06-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="efd06-112">Row index:</span></span>  <br/> |<span data-ttu-id="efd06-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="efd06-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="efd06-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="efd06-114">Cell index:</span></span>  <br/> |<span data-ttu-id="efd06-115">**visSketchEnabled**</span><span class="sxs-lookup"><span data-stu-id="efd06-115">**visSketchEnabled**</span></span> <br/> |
   

