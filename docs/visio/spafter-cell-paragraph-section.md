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
ms.openlocfilehash: 93db93e58124b5f176fb57f843580eff6a3d4d3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806573"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="8a278-103">[SpAfter] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="8a278-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="8a278-104">図形のテキスト ブロック内にある各段落の後に挿入する間隔を指定します。この値に、[SpLine] セルや [BottomMargin] セル (テキスト ブロックの最後の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a278-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a278-105">備考</span><span class="sxs-lookup"><span data-stu-id="8a278-105">Remarks</span></span>

<span data-ttu-id="8a278-p101">この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、[SpAfter] の設定は変わりません。</span><span class="sxs-lookup"><span data-stu-id="8a278-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="8a278-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [spafter] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="8a278-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8a278-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="8a278-109">Cell name:</span></span>  <br/> | <span data-ttu-id="8a278-110">Para.SpAfter [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="8a278-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8a278-111">プログラムから、インデックスによって [spafter] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8a278-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8a278-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8a278-112">Section index:</span></span>  <br/> |<span data-ttu-id="8a278-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8a278-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="8a278-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8a278-114">Row index:</span></span>  <br/> |<span data-ttu-id="8a278-115">**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="8a278-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8a278-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8a278-116">Cell index:</span></span>  <br/> |<span data-ttu-id="8a278-117">**visSpaceAfter**</span><span class="sxs-lookup"><span data-stu-id="8a278-117">**visSpaceAfter**</span></span> <br/> |
   

