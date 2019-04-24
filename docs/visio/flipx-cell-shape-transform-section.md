---
title: '[FlipX] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: 図形が左右反転されているかを示します。
ms.openlocfilehash: b7a4a15e5a7759eddcda3ec391a81f14df545691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346187"
---
# <a name="flipx-cell-shape-transform-section"></a><span data-ttu-id="8619b-103">[FlipX] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="8619b-103">FlipX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="8619b-104">図形が左右反転されているかを示します。</span><span class="sxs-lookup"><span data-stu-id="8619b-104">Indicates whether the shape has been flipped horizontally.</span></span>
  
|<span data-ttu-id="8619b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="8619b-105">**Value**</span></span>|<span data-ttu-id="8619b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="8619b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8619b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8619b-107">TRUE</span></span>  <br/> | <span data-ttu-id="8619b-108">図形は左右反転されています。</span><span class="sxs-lookup"><span data-stu-id="8619b-108">The shape has been flipped horizontally.</span></span>  <br/> |
| <span data-ttu-id="8619b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8619b-109">FALSE</span></span>  <br/> | <span data-ttu-id="8619b-110">図形は左右反転されていません。</span><span class="sxs-lookup"><span data-stu-id="8619b-110">The shape has not been flipped horizontally.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8619b-111">解説</span><span class="sxs-lookup"><span data-stu-id="8619b-111">Remarks</span></span>

<span data-ttu-id="8619b-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FlipX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8619b-112">To get a reference to the FlipX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8619b-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="8619b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="8619b-114">[flipx]</span><span class="sxs-lookup"><span data-stu-id="8619b-114">FlipX</span></span>  <br/> |
   
<span data-ttu-id="8619b-115">プログラムから、インデックスによって [FlipX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8619b-115">To get a reference to the FlipX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8619b-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8619b-116">Section index:</span></span>  <br/> |<span data-ttu-id="8619b-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8619b-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8619b-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8619b-118">Row index:</span></span>  <br/> |<span data-ttu-id="8619b-119">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="8619b-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="8619b-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8619b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8619b-121">**visXFormFlipX**</span><span class="sxs-lookup"><span data-stu-id="8619b-121">**visXFormFlipX**</span></span> <br/> |
   

