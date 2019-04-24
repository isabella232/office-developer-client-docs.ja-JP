---
title: '[SpBefore] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: 図形のテキスト ブロック内にある各段落の前に挿入する間隔を指定します。この値に、[SpLine] セルや [TopMargin] セル (テキスト ブロックの最初の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329884"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="69da5-103">[SpBefore] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="69da5-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="69da5-104">図形のテキスト ブロック内にある各段落の前に挿入する間隔を指定します。この値に、[SpLine] セルや [TopMargin] セル (テキスト ブロックの最初の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。</span><span class="sxs-lookup"><span data-stu-id="69da5-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69da5-105">解説</span><span class="sxs-lookup"><span data-stu-id="69da5-105">Remarks</span></span>

<span data-ttu-id="69da5-p101">この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、[SpBefore] の設定は変わりません。</span><span class="sxs-lookup"><span data-stu-id="69da5-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="69da5-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SpBefore] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="69da5-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="69da5-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="69da5-109">Cell name:</span></span>  <br/> | <span data-ttu-id="69da5-110">段落前 [ *i* ] ( *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="69da5-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="69da5-111">プログラムから、インデックスによって [SpBefore] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="69da5-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="69da5-112">セクション インデックス :</span><span class="sxs-lookup"><span data-stu-id="69da5-112">Section index:</span></span>  <br/> |<span data-ttu-id="69da5-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="69da5-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="69da5-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="69da5-114">Row index:</span></span>  <br/> |<span data-ttu-id="69da5-115">**visRowParagraph** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="69da5-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="69da5-116">セル インデックス :</span><span class="sxs-lookup"><span data-stu-id="69da5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="69da5-117">**visSpaceBefore**</span><span class="sxs-lookup"><span data-stu-id="69da5-117">**visSpaceBefore**</span></span> <br/> |
   

