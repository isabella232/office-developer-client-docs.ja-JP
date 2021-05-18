---
title: '[ReflectionSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: 図形と相対する反射のサイズを、0.0 から 100.0% までのパーセンテージとして決定します。[ReflectionSize] セルに 0% の値を設定した図形には反射がありません。100% の値を設定すると、図形の完全な鏡像が表示されます。
ms.openlocfilehash: 60fcb315ec1b6187082bdcdbbdcfaa4b80bbcfb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409077"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a><span data-ttu-id="f295c-104">[ReflectionSize] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="f295c-104">ReflectionSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="f295c-p102">図形と相対する反射のサイズを、0.0 から 100.0% までのパーセンテージとして決定します。[**ReflectionSize**] セルに 0% の値を設定した図形には反射がありません。100% の値を設定すると、図形の完全な鏡像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f295c-p102">Determines the size of the reflection relative to the shape, as a percentage from 0.0 to 100.0%. A shape with a value of 0% in the **ReflectionSize** cell does not have a reflection; a value of 100% displays a complete mirror image of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f295c-107">注釈</span><span class="sxs-lookup"><span data-stu-id="f295c-107">Remarks</span></span>

<span data-ttu-id="f295c-108">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ReflectionSize**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f295c-108">To get a reference to the **ReflectionSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f295c-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="f295c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="f295c-110">ReflectionSize</span><span class="sxs-lookup"><span data-stu-id="f295c-110">ReflectionSize</span></span>  <br/> |
   
<span data-ttu-id="f295c-111">プログラムから、インデックスによって [**ReflectionSize**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f295c-111">To get a reference to the **ReflectionSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f295c-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f295c-112">Section index:</span></span>  <br/> |<span data-ttu-id="f295c-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f295c-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f295c-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f295c-114">Row index:</span></span>  <br/> |<span data-ttu-id="f295c-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="f295c-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="f295c-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f295c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f295c-117">**visReflectionSize**</span><span class="sxs-lookup"><span data-stu-id="f295c-117">**visReflectionSize**</span></span> <br/> |
   

