---
title: '[ReflectionSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: 図形を基準にした反射のサイズを、0.0 ~ 100.0% の割合で指定します。 [reflectionsize] セルの値が 0% の図形には反射がありません。100% の値を指定すると、図形の完全なミラーイメージが表示されます。
ms.openlocfilehash: 60fcb315ec1b6187082bdcdbbdcfaa4b80bbcfb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348357"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a><span data-ttu-id="1b144-104">[ReflectionSize] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="1b144-104">ReflectionSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="1b144-105">図形を基準にした反射のサイズを、0.0 ~ 100.0% の割合で指定します。</span><span class="sxs-lookup"><span data-stu-id="1b144-105">Determines the size of the reflection relative to the shape, as a percentage from 0.0 to 100.0%.</span></span> <span data-ttu-id="1b144-106">**[reflectionsize]** セルの値が 0% の図形には反射がありません。100% の値を指定すると、図形の完全なミラーイメージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1b144-106">A shape with a value of 0% in the **ReflectionSize** cell does not have a reflection; a value of 100% displays a complete mirror image of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1b144-107">解説</span><span class="sxs-lookup"><span data-stu-id="1b144-107">Remarks</span></span>

<span data-ttu-id="1b144-108">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ReflectionSize**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b144-108">To get a reference to the **ReflectionSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1b144-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="1b144-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1b144-110">[reflectionsize]</span><span class="sxs-lookup"><span data-stu-id="1b144-110">ReflectionSize</span></span>  <br/> |
   
<span data-ttu-id="1b144-111">プログラムから、インデックスによって [**ReflectionSize**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b144-111">To get a reference to the **ReflectionSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1b144-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1b144-112">Section index:</span></span>  <br/> |<span data-ttu-id="1b144-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1b144-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1b144-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1b144-114">Row index:</span></span>  <br/> |<span data-ttu-id="1b144-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="1b144-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="1b144-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1b144-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1b144-117">**visReflectionSize**</span><span class="sxs-lookup"><span data-stu-id="1b144-117">**visReflectionSize**</span></span> <br/> |
   

