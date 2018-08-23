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
ms.openlocfilehash: f3515485b0418ffeaf55910a972e1e480f428e4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804924"
---
# <a name="bottommargin-cell-text-block-format-section"></a><span data-ttu-id="33c51-106">[BottomMargin] セル ([テキスト ブロックの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="33c51-106">BottomMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="33c51-p102">テキスト ブロックの下の枠線からそのテキスト ブロックに含まれるテキストの最終行までの距離を指定します。既定値は 0.1 インチです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、下余白の長さは変わりません。</span><span class="sxs-lookup"><span data-stu-id="33c51-p102">Determines the distance between the bottom border of the text block and the last line of text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the bottom margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="33c51-111">備考</span><span class="sxs-lookup"><span data-stu-id="33c51-111">Remarks</span></span>

<span data-ttu-id="33c51-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BottomMargin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="33c51-112">To get a reference to the BottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33c51-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="33c51-113">Cell name:</span></span>  <br/> | <span data-ttu-id="33c51-114">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="33c51-114">BottomMargin</span></span>  <br/> |
   
<span data-ttu-id="33c51-115">プログラムから、インデックスによって [BottomMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="33c51-115">To get a reference to the BottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33c51-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="33c51-116">Section index:</span></span>  <br/> |<span data-ttu-id="33c51-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="33c51-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="33c51-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="33c51-118">Row index:</span></span>  <br/> |<span data-ttu-id="33c51-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="33c51-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="33c51-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="33c51-120">Cell index:</span></span>  <br/> |<span data-ttu-id="33c51-121">**visTxtBlkBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="33c51-121">**visTxtBlkBottomMargin**</span></span> <br/> |
   

