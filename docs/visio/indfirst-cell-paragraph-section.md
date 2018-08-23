---
title: '[IndFirst] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: 図形のテキスト ブロック内にある各段落の先頭行について、段落の左インデントからインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、先頭行のインデントは変わりません。
ms.openlocfilehash: 03c34a0ccd1681d3523d743ebfc34af7b9dcfa87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805569"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="c8871-105">[IndFirst] セル ([段落] セクション)</span><span class="sxs-lookup"><span data-stu-id="c8871-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="c8871-p102">図形のテキスト ブロック内にある各段落の先頭行について、段落の左インデントからインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、先頭行のインデントは変わりません。</span><span class="sxs-lookup"><span data-stu-id="c8871-p102">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph. This value is independent of the scale of the drawing. If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8871-109">備考</span><span class="sxs-lookup"><span data-stu-id="c8871-109">Remarks</span></span>

<span data-ttu-id="c8871-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IndFirst] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c8871-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8871-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="c8871-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c8871-112">Para.IndFirst [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="c8871-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c8871-113">プログラムから、インデックスによって [IndFirst] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c8871-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8871-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8871-114">Section index:</span></span>  <br/> |<span data-ttu-id="c8871-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="c8871-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="c8871-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8871-116">Row index:</span></span>  <br/> |<span data-ttu-id="c8871-117">**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="c8871-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c8871-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8871-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c8871-119">**visIndentFirst**</span><span class="sxs-lookup"><span data-stu-id="c8871-119">**visIndentFirst**</span></span> <br/> |
   

