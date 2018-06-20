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
ms.openlocfilehash: fc014ff6c5a3650361d6afd478a5858f84fb5c47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805412"
---
# <a name="flipx-cell-shape-transform-section"></a><span data-ttu-id="c6666-103">[FlipX] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="c6666-103">FlipX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="c6666-104">図形が左右反転されているかを示します。</span><span class="sxs-lookup"><span data-stu-id="c6666-104">Indicates whether the shape has been flipped horizontally.</span></span>
  
|<span data-ttu-id="c6666-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c6666-105">**Value**</span></span>|<span data-ttu-id="c6666-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="c6666-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c6666-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c6666-107">TRUE</span></span>  <br/> | <span data-ttu-id="c6666-108">図形は左右反転されています。</span><span class="sxs-lookup"><span data-stu-id="c6666-108">The shape has been flipped horizontally.</span></span>  <br/> |
| <span data-ttu-id="c6666-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6666-109">FALSE</span></span>  <br/> | <span data-ttu-id="c6666-110">図形は左右反転されていません。</span><span class="sxs-lookup"><span data-stu-id="c6666-110">The shape has not been flipped horizontally.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6666-111">備考</span><span class="sxs-lookup"><span data-stu-id="c6666-111">Remarks</span></span>

<span data-ttu-id="c6666-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [flipx] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="c6666-112">To get a reference to the FlipX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6666-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="c6666-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c6666-114">[Flipx]</span><span class="sxs-lookup"><span data-stu-id="c6666-114">FlipX</span></span>  <br/> |
   
<span data-ttu-id="c6666-115">プログラムから、インデックスによって [flipx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c6666-115">To get a reference to the FlipX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6666-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c6666-116">Section index:</span></span>  <br/> |<span data-ttu-id="c6666-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c6666-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c6666-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c6666-118">Row index:</span></span>  <br/> |<span data-ttu-id="c6666-119">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="c6666-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="c6666-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c6666-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c6666-121">**visXFormFlipX**</span><span class="sxs-lookup"><span data-stu-id="c6666-121">**visXFormFlipX**</span></span> <br/> |
   

