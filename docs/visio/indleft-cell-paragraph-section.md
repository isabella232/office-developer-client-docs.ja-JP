---
title: '[IndLeft] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: 段落にあるテキストのすべての行について、テキスト ブロックの左余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左インデントは変わりません。
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805578"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="160d0-105">[IndLeft] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="160d0-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="160d0-p102">段落にあるテキストのすべての行について、テキスト ブロックの左余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左インデントは変わりません。</span><span class="sxs-lookup"><span data-stu-id="160d0-p102">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="160d0-109">備考</span><span class="sxs-lookup"><span data-stu-id="160d0-109">Remarks</span></span>

<span data-ttu-id="160d0-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [indleft] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="160d0-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="160d0-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="160d0-111">Cell name:</span></span>  <br/> | <span data-ttu-id="160d0-112">Para.IndLeft [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="160d0-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="160d0-113">プログラムから、インデックスによって [indleft] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="160d0-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="160d0-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="160d0-114">Section index:</span></span>  <br/> |<span data-ttu-id="160d0-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="160d0-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="160d0-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="160d0-116">Row index:</span></span>  <br/> |<span data-ttu-id="160d0-117">**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="160d0-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="160d0-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="160d0-118">Cell index:</span></span>  <br/> |<span data-ttu-id="160d0-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="160d0-119">**visIndentLeft**</span></span> <br/> |
   
