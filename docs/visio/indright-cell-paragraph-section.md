---
title: '[IndRight] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: 段落にあるテキストのすべての行について、テキスト ブロックの右余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右インデントは変わりません。
ms.openlocfilehash: 83f2688e598ffb335a9fafd1eed56ea17ffd4b2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805580"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="8113d-105">[IndRight] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="8113d-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="8113d-p102">段落にあるテキストのすべての行について、テキスト ブロックの右余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右インデントは変わりません。</span><span class="sxs-lookup"><span data-stu-id="8113d-p102">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8113d-109">備考</span><span class="sxs-lookup"><span data-stu-id="8113d-109">Remarks</span></span>

<span data-ttu-id="8113d-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [indright] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="8113d-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8113d-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="8113d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="8113d-112">Para.IndRight [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="8113d-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8113d-113">プログラムから、インデックスによって [indright] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8113d-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8113d-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8113d-114">Section index:</span></span>  <br/> |<span data-ttu-id="8113d-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8113d-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="8113d-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8113d-116">Row index:</span></span>  <br/> |<span data-ttu-id="8113d-117">**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="8113d-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8113d-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8113d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="8113d-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="8113d-119">**visIndentRight**</span></span> <br/> |
   

