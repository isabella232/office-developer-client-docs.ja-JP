---
title: '[BevelTopWidth] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4eae2c4e-ac49-47d5-8b55-71da06ccbf49
description: 上面取りの幅をポイント単位で指定します。
ms.openlocfilehash: 6c59a23fcfd39ff7c3420e63607ecc98b46d40be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284456"
---
# <a name="beveltopwidth-cell-bevel-properties-section"></a><span data-ttu-id="258d9-103">[BevelTopWidth] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="258d9-103">BevelTopWidth Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="258d9-104">上面取りの幅をポイント単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="258d9-104">Determines the width of the top bevel in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="258d9-105">解説</span><span class="sxs-lookup"><span data-stu-id="258d9-105">Remarks</span></span>

<span data-ttu-id="258d9-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [傾斜] [**幅**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="258d9-106">To get a reference to the **BevelTopWidth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="258d9-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="258d9-107">Cell name:</span></span>  <br/> | <span data-ttu-id="258d9-108">[beveltopwidth]</span><span class="sxs-lookup"><span data-stu-id="258d9-108">BevelTopWidth</span></span>  <br/> |
   
<span data-ttu-id="258d9-109">プログラムから、インデックスによって [**傾斜 eltopwidth** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="258d9-109">To get a reference to the **BevelTopWidth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="258d9-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="258d9-110">Section index:</span></span>  <br/> |<span data-ttu-id="258d9-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="258d9-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="258d9-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="258d9-112">Row index:</span></span>  <br/> |<span data-ttu-id="258d9-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="258d9-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="258d9-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="258d9-114">Cell index:</span></span>  <br/> |<span data-ttu-id="258d9-115">**visBevelTopWidth**</span><span class="sxs-lookup"><span data-stu-id="258d9-115">**visBevelTopWidth**</span></span> <br/> |
   

