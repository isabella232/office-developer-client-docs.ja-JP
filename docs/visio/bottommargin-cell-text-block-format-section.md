---
title: '[BottomMargin] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm120
localization_priority: Normal
ms.assetid: 3121911b-34d5-d99c-3806-76f6e2824f92
description: テキスト ブロックの下の枠線からそのテキスト ブロックに含まれるテキストの最終行までの距離を指定します。既定値は 0.1 インチです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、下余白の長さは変わりません。
ms.openlocfilehash: 544557f1e797315619bc9975db0b87a09981726c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417211"
---
# <a name="bottommargin-cell-text-block-format-section"></a><span data-ttu-id="cc5e8-106">[BottomMargin] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="cc5e8-106">BottomMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="cc5e8-p102">テキスト ブロックの下の枠線からそのテキスト ブロックに含まれるテキストの最終行までの距離を指定します。既定値は 0.1 インチです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、下余白の長さは変わりません。</span><span class="sxs-lookup"><span data-stu-id="cc5e8-p102">Determines the distance between the bottom border of the text block and the last line of text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the bottom margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc5e8-111">注釈</span><span class="sxs-lookup"><span data-stu-id="cc5e8-111">Remarks</span></span>

<span data-ttu-id="cc5e8-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BottomMargin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cc5e8-112">To get a reference to the BottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc5e8-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="cc5e8-113">Cell name:</span></span>  <br/> | <span data-ttu-id="cc5e8-114">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="cc5e8-114">BottomMargin</span></span>  <br/> |
   
<span data-ttu-id="cc5e8-115">プログラムから、インデックスによって [BottomMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cc5e8-115">To get a reference to the BottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc5e8-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc5e8-116">Section index:</span></span>  <br/> |<span data-ttu-id="cc5e8-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cc5e8-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc5e8-118">Row index:</span></span>  <br/> |<span data-ttu-id="cc5e8-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="cc5e8-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc5e8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="cc5e8-121">**visTxtBlkBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-121">**visTxtBlkBottomMargin**</span></span> <br/> |
   

