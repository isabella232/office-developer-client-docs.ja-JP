---
title: '[SpAfter] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: 図形のテキスト ブロック内にある各段落の後に挿入する間隔を指定します。この値に、[SpLine] セルや [BottomMargin] セル (テキスト ブロックの最後の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。
ms.openlocfilehash: 2b8fe7e2b0df09561d0db4367f917c8f4b71335d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335225"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="775e4-103">[SpAfter] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="775e4-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="775e4-104">図形のテキスト ブロック内にある各段落の後に挿入する間隔を指定します。この値に、[SpLine] セルや [BottomMargin] セル (テキスト ブロックの最後の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。</span><span class="sxs-lookup"><span data-stu-id="775e4-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="775e4-105">解説</span><span class="sxs-lookup"><span data-stu-id="775e4-105">Remarks</span></span>

<span data-ttu-id="775e4-p101">この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、[SpAfter] の設定は変わりません。</span><span class="sxs-lookup"><span data-stu-id="775e4-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="775e4-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SpAfter] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="775e4-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="775e4-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="775e4-109">Cell name:</span></span>  <br/> | <span data-ttu-id="775e4-110"><1> の後、spafter、 \*\* 2、3... \*\*</span><span class="sxs-lookup"><span data-stu-id="775e4-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="775e4-111">プログラムから、インデックスによって [SpAfter] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="775e4-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="775e4-112">セクション インデックス :</span><span class="sxs-lookup"><span data-stu-id="775e4-112">Section index:</span></span>  <br/> |<span data-ttu-id="775e4-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="775e4-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="775e4-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="775e4-114">Row index:</span></span>  <br/> |<span data-ttu-id="775e4-115">**visRowParagraph** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="775e4-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="775e4-116">セル インデックス :</span><span class="sxs-lookup"><span data-stu-id="775e4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="775e4-117">**visSpaceAfter**</span><span class="sxs-lookup"><span data-stu-id="775e4-117">**visSpaceAfter**</span></span> <br/> |
   

