---
title: '[BevelContourSize] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ebde552-f1e6-43d0-8704-4e29eb2b1c9d
description: 傾斜面の輪郭をポイント単位でのサイズを決定します。
ms.openlocfilehash: 1b7a83674492d5ea8d3fae8150e995fd8511eef0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804814"
---
# <a name="bevelcontoursize-cell-bevel-properties-section"></a><span data-ttu-id="824fc-103">[BevelContourSize] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="824fc-103">BevelContourSize Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="824fc-104">傾斜面の輪郭をポイント単位でのサイズを決定します。</span><span class="sxs-lookup"><span data-stu-id="824fc-104">Determines the size of the bevel's contour in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="824fc-105">備考</span><span class="sxs-lookup"><span data-stu-id="824fc-105">Remarks</span></span>

<span data-ttu-id="824fc-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelContourSize** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="824fc-106">To get a reference to the **BevelContourSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="824fc-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="824fc-107">Cell name:</span></span>  <br/> | <span data-ttu-id="824fc-108">BevelContourSize</span><span class="sxs-lookup"><span data-stu-id="824fc-108">BevelContourSize</span></span>  <br/> |
   
<span data-ttu-id="824fc-109">プログラムから、インデックスによって [ **BevelContourSize** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="824fc-109">To get a reference to the **BevelContourSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="824fc-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="824fc-110">Section index:</span></span>  <br/> |<span data-ttu-id="824fc-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="824fc-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="824fc-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="824fc-112">Row index:</span></span>  <br/> |<span data-ttu-id="824fc-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="824fc-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="824fc-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="824fc-114">Cell index:</span></span>  <br/> |<span data-ttu-id="824fc-115">**visBevelContourSize**</span><span class="sxs-lookup"><span data-stu-id="824fc-115">**visBevelContourSize**</span></span> <br/> |
   

