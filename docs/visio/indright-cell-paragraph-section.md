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
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335344"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="f7309-105">[IndRight] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="f7309-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="f7309-p102">段落にあるテキストのすべての行について、テキスト ブロックの右余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右インデントは変わりません。</span><span class="sxs-lookup"><span data-stu-id="f7309-p102">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7309-109">解説</span><span class="sxs-lookup"><span data-stu-id="f7309-109">Remarks</span></span>

<span data-ttu-id="f7309-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IndRight] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f7309-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7309-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="f7309-111">Cell name:</span></span>  <br/> | <span data-ttu-id="f7309-112">[indright] [ *i* ] *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="f7309-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f7309-113">プログラムから、インデックスによって [IndRight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7309-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7309-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f7309-114">Section index:</span></span>  <br/> |<span data-ttu-id="f7309-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="f7309-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="f7309-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f7309-116">Row index:</span></span>  <br/> |<span data-ttu-id="f7309-117">**visRowParagraph** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="f7309-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f7309-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f7309-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f7309-119">**visindentright**</span><span class="sxs-lookup"><span data-stu-id="f7309-119">**visIndentRight**</span></span> <br/> |
   

