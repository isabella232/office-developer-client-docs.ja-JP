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
ms.openlocfilehash: aa6d9fd14a40f4fe6b269d9750f603d8faf1d550
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410323"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="e860c-105">[IndFirst] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="e860c-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="e860c-p102">図形のテキスト ブロック内にある各段落の先頭行について、段落の左インデントからインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、先頭行のインデントは変わりません。</span><span class="sxs-lookup"><span data-stu-id="e860c-p102">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph. This value is independent of the scale of the drawing. If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e860c-109">注釈</span><span class="sxs-lookup"><span data-stu-id="e860c-109">Remarks</span></span>

<span data-ttu-id="e860c-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IndFirst] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e860c-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e860c-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="e860c-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e860c-112"><1>、2、3のように\*\* 、最初に [ *i* ] を指定します。</span><span class="sxs-lookup"><span data-stu-id="e860c-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e860c-113">プログラムから、インデックスによって [IndFirst] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e860c-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e860c-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e860c-114">Section index:</span></span>  <br/> |<span data-ttu-id="e860c-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="e860c-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="e860c-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e860c-116">Row index:</span></span>  <br/> |<span data-ttu-id="e860c-117">**visRowParagraph** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="e860c-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e860c-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e860c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e860c-119">**visindentfirst**</span><span class="sxs-lookup"><span data-stu-id="e860c-119">**visIndentFirst**</span></span> <br/> |
   

