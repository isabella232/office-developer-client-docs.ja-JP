---
title: '[BevelTopHeight] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b09b48d0-9008-4e43-9506-93a830ad9452
description: 図形の上面取りの高さをポイント単位で指定します。
ms.openlocfilehash: 4da2fd1d61b530450f9020b12d5016015fd59dba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315737"
---
# <a name="beveltopheight-cell-bevel-properties-section"></a><span data-ttu-id="aa229-103">[BevelTopHeight] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="aa229-103">BevelTopHeight Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="aa229-104">図形の上面取りの高さをポイント単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="aa229-104">Determines the height of a shape's top bevel in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aa229-105">解説</span><span class="sxs-lookup"><span data-stu-id="aa229-105">Remarks</span></span>

<span data-ttu-id="aa229-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [傾斜] [**高さ**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="aa229-106">To get a reference to the **BevelTopHeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aa229-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="aa229-107">Cell name:</span></span>  <br/> | <span data-ttu-id="aa229-108">[beveltopheight]</span><span class="sxs-lookup"><span data-stu-id="aa229-108">BevelTopHeight</span></span>  <br/> |
   
<span data-ttu-id="aa229-109">プログラムから、インデックスによって [傾斜] [**高さ**] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="aa229-109">To get a reference to the **BevelTopHeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aa229-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="aa229-110">Section index:</span></span>  <br/> |<span data-ttu-id="aa229-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aa229-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aa229-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="aa229-112">Row index:</span></span>  <br/> |<span data-ttu-id="aa229-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="aa229-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="aa229-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="aa229-114">Cell index:</span></span>  <br/> |<span data-ttu-id="aa229-115">**visBevelTopHeight**</span><span class="sxs-lookup"><span data-stu-id="aa229-115">**visBevelTopHeight**</span></span> <br/> |
   

