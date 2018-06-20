---
title: '[Comment] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: コメント内に表示されるテキストが含まれます。
ms.openlocfilehash: 443a229058a9ca910ba5b38b093706c9c2e3e95b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805028"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="2f4f4-103">[Comment] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="2f4f4-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="2f4f4-104">コメント内に表示されるテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2f4f4-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2f4f4-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くときにのみ、または .vsd ファイルの形式で .vsdx ファイルを保存するときにコメントを追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f4f4-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="2f4f4-106">Visio 2013 で .vsdx のドキュメント内のコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="2f4f4-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2f4f4-107">備考</span><span class="sxs-lookup"><span data-stu-id="2f4f4-107">Remarks</span></span>

<span data-ttu-id="2f4f4-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Comment] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="2f4f4-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f4f4-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="2f4f4-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2f4f4-110">Annotation.Comment [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="2f4f4-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2f4f4-111">プログラムから、インデックスによって [Comment] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="2f4f4-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f4f4-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f4f4-112">Section index:</span></span>  <br/> |<span data-ttu-id="2f4f4-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="2f4f4-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="2f4f4-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f4f4-114">Row index:</span></span>  <br/> |<span data-ttu-id="2f4f4-115">**visRowAnnotation** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="2f4f4-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2f4f4-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f4f4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2f4f4-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="2f4f4-117">**visAnnotationComment**</span></span> <br/> |
   

