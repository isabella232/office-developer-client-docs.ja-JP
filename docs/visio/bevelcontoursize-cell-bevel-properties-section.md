---
title: '[BevelContourSize] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ebde552-f1e6-43d0-8704-4e29eb2b1c9d
description: 面取りの輪郭のサイズをポイント単位で指定します。
ms.openlocfilehash: bb37c1a9990e1ee4bcca917f065b7872b8ae3bd7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285127"
---
# <a name="bevelcontoursize-cell-bevel-properties-section"></a><span data-ttu-id="41395-103">[BevelContourSize] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="41395-103">BevelContourSize Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="41395-104">面取りの輪郭のサイズをポイント単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="41395-104">Determines the size of the bevel's contour in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="41395-105">解説</span><span class="sxs-lookup"><span data-stu-id="41395-105">Remarks</span></span>

<span data-ttu-id="41395-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [傾斜] [ **oursize** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="41395-106">To get a reference to the **BevelContourSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41395-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="41395-107">Cell name:</span></span>  <br/> | <span data-ttu-id="41395-108">[bevelcontoursize]</span><span class="sxs-lookup"><span data-stu-id="41395-108">BevelContourSize</span></span>  <br/> |
   
<span data-ttu-id="41395-109">プログラムから、インデックスによって [**傾斜 elクレヨン oursize** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="41395-109">To get a reference to the **BevelContourSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41395-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="41395-110">Section index:</span></span>  <br/> |<span data-ttu-id="41395-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41395-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="41395-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="41395-112">Row index:</span></span>  <br/> |<span data-ttu-id="41395-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="41395-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="41395-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="41395-114">Cell index:</span></span>  <br/> |<span data-ttu-id="41395-115">**visBevelContourSize**</span><span class="sxs-lookup"><span data-stu-id="41395-115">**visBevelContourSize**</span></span> <br/> |
   

