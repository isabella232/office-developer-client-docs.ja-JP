---
title: '[ReflectionSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: 0.0 から 100.0% の割合として、図形を基準にして反射のサイズを決定します。 ReflectionSize のセルに 0% の値を持つ図形には、リフレクションはありません。100% の値は、図形の完全なミラー イメージを表示します。
ms.openlocfilehash: b525a5f7379b2702dd7152d4eccf6dab1879a6cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806165"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a><span data-ttu-id="14dd7-104">[ReflectionSize] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="14dd7-104">ReflectionSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="14dd7-105">0.0 から 100.0% の割合として、図形を基準にして反射のサイズを決定します。</span><span class="sxs-lookup"><span data-stu-id="14dd7-105">Determines the size of the reflection relative to the shape, as a percentage from 0.0 to 100.0%.</span></span> <span data-ttu-id="14dd7-106">**ReflectionSize**のセルに 0% の値を持つ図形には、リフレクションはありません。100% の値は、図形の完全なミラー イメージを表示します。</span><span class="sxs-lookup"><span data-stu-id="14dd7-106">A shape with a value of 0% in the **ReflectionSize** cell does not have a reflection; a value of 100% displays a complete mirror image of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="14dd7-107">備考</span><span class="sxs-lookup"><span data-stu-id="14dd7-107">Remarks</span></span>

<span data-ttu-id="14dd7-108">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReflectionSize** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="14dd7-108">To get a reference to the **ReflectionSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14dd7-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="14dd7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="14dd7-110">ReflectionSize</span><span class="sxs-lookup"><span data-stu-id="14dd7-110">ReflectionSize</span></span>  <br/> |
   
<span data-ttu-id="14dd7-111">プログラムから、インデックスによって [ **ReflectionSize** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="14dd7-111">To get a reference to the **ReflectionSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14dd7-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="14dd7-112">Section index:</span></span>  <br/> |<span data-ttu-id="14dd7-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="14dd7-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="14dd7-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="14dd7-114">Row index:</span></span>  <br/> |<span data-ttu-id="14dd7-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="14dd7-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="14dd7-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="14dd7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="14dd7-117">**visReflectionSize**</span><span class="sxs-lookup"><span data-stu-id="14dd7-117">**visReflectionSize**</span></span> <br/> |
   

