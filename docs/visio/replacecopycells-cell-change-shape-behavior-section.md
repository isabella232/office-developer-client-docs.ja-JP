---
title: '[ReplaceCopyCells] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: 図形の置換操作中に、古い図形から置換後の図形にコピーされるシェイプシート内のセル一覧を示します。
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806189"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="94d43-103">[ReplaceCopyCells] セル ([図形の動作の変更] セクション)</span><span class="sxs-lookup"><span data-stu-id="94d43-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="94d43-104">図形の置換操作中に、古い図形から置換後の図形にコピーされるシェイプシート内のセル一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="94d43-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="94d43-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="94d43-105">Remarks</span></span>

<span data-ttu-id="94d43-106">交換用のマスター シェイプには、 **ReplaceCopyCells**のセル、セルへの参照、関数の各引数である**DEPENDSON**関数呼び出しを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="94d43-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="94d43-107">それらのセルは、古い図形から、図形のシェイプ シートになっているに関係なく、図形の置換操作の結果にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="94d43-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="94d43-p102">他のセルを参照する値および/または数式は、作成した図形にコピーされます。作成した図形に参照先のセルがない場合、コピーされたセルには値のみが格納されます。</span><span class="sxs-lookup"><span data-stu-id="94d43-p102">Values and/or formulas that reference other cells are copied to the resulting shape. If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="94d43-110">**ReplaceCopyCells**セルの参照は、セル**保護**] セクションと、 **ReplaceLockFormat**、 **ReplaceLockShapeData**、および**ReplaceLockText**セルで定義されている保護の設定をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="94d43-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="94d43-111">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReplaceCopyCells** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="94d43-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94d43-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="94d43-112">Cell name:</span></span>  <br/> | <span data-ttu-id="94d43-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="94d43-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="94d43-114">プログラムから、インデックスによって [ **ReplaceCopyCells** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="94d43-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94d43-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="94d43-115">Section index:</span></span>  <br/> |<span data-ttu-id="94d43-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="94d43-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="94d43-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="94d43-117">Row index:</span></span>  <br/> |<span data-ttu-id="94d43-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="94d43-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="94d43-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="94d43-119">Cell index:</span></span>  <br/> |<span data-ttu-id="94d43-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="94d43-120">**visReplaceCopyCells**</span></span> <br/> |
   

