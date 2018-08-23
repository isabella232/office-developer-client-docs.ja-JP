---
title: '[TopMargin] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1015
localization_priority: Normal
ms.assetid: c599b444-4d0e-a855-b04b-dd9dcaedf263
description: テキスト ブロックの上の枠線から、そのブロックに含まれるテキストの最初の行までの間隔を指定します。既定値は 4.0000 ポイントです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、上余白の長さは変わりません。
ms.openlocfilehash: 71e8e3b41dc9c59c374111dcd442e55ab70330fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806684"
---
# <a name="topmargin-cell-text-block-format-section"></a><span data-ttu-id="3096f-106">[TopMargin] セル ([テキスト ブロックの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="3096f-106">TopMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="3096f-p102">テキスト ブロックの上の枠線から、そのブロックに含まれるテキストの最初の行までの間隔を指定します。既定値は 4.0000 ポイントです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、上余白の長さは変わりません。</span><span class="sxs-lookup"><span data-stu-id="3096f-p102">Determines the distance between the top border of the text block and the first line of text it contains. The default is 4.0000 point. This value is independent of the scale of the drawing. If the drawing is scaled, the top margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3096f-111">備考</span><span class="sxs-lookup"><span data-stu-id="3096f-111">Remarks</span></span>

<span data-ttu-id="3096f-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TopMargin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3096f-112">To get a reference to the TopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3096f-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="3096f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3096f-114">TopMargin</span><span class="sxs-lookup"><span data-stu-id="3096f-114">TopMargin</span></span>  <br/> |
   
<span data-ttu-id="3096f-115">プログラムから、インデックスによって [TopMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3096f-115">To get a reference to the TopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3096f-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3096f-116">Section index:</span></span>  <br/> |<span data-ttu-id="3096f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3096f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3096f-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3096f-118">Row index:</span></span>  <br/> |<span data-ttu-id="3096f-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="3096f-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="3096f-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3096f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3096f-121">**visTxtBlkTopMargin**</span><span class="sxs-lookup"><span data-stu-id="3096f-121">**visTxtBlkTopMargin**</span></span> <br/> |
   

