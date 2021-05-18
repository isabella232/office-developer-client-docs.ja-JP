---
title: '[LeftMargin] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: テキスト ブロックの左枠からそのブロックに含まれるテキストまでの距離を指定します。既定値は 0.1 インチです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左余白の長さは変わりません。
ms.openlocfilehash: fee8eca8b5730e40518babe0c76549e10bebd902
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411338"
---
# <a name="leftmargin-cell-text-block-format-section"></a><span data-ttu-id="7d6b8-106">[LeftMargin] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="7d6b8-106">LeftMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="7d6b8-p102">テキスト ブロックの左枠からそのブロックに含まれるテキストまでの距離を指定します。既定値は 0.1 インチです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左余白の長さは変わりません。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-p102">Determines the distance between the left border of the text block and the text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the left margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d6b8-111">注釈</span><span class="sxs-lookup"><span data-stu-id="7d6b8-111">Remarks</span></span>

<span data-ttu-id="7d6b8-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LeftMargin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-112">To get a reference to the LeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d6b8-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="7d6b8-113">Cell name:</span></span>  <br/> | <span data-ttu-id="7d6b8-114">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="7d6b8-114">LeftMargin</span></span>  <br/> |
   
<span data-ttu-id="7d6b8-115">プログラムから、インデックスによって [LeftMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-115">To get a reference to the LeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d6b8-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7d6b8-116">Section index:</span></span>  <br/> |<span data-ttu-id="7d6b8-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7d6b8-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7d6b8-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7d6b8-118">Row index:</span></span>  <br/> |<span data-ttu-id="7d6b8-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="7d6b8-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="7d6b8-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7d6b8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="7d6b8-121">**visTxtBlkLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="7d6b8-121">**visTxtBlkLeftMargin**</span></span> <br/> |
   

