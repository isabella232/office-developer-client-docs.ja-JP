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
ms.openlocfilehash: fd9dce2618c0b8c967b794b0beea8b772a231003
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359039"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="57d95-103">[Comment] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="57d95-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="57d95-104">コメント内に表示されるテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="57d95-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="57d95-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くとき、または .vsd ファイル形式で .vsdx ファイルを保存するときにのみ、コメントの追跡に使用されます。</span><span class="sxs-lookup"><span data-stu-id="57d95-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="57d95-106">これは、Visio 2013 の .vsdx ドキュメントでコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="57d95-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="57d95-107">解説</span><span class="sxs-lookup"><span data-stu-id="57d95-107">Remarks</span></span>

<span data-ttu-id="57d95-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Comment] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="57d95-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="57d95-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="57d95-109">Cell name:</span></span>  <br/> | <span data-ttu-id="57d95-110">コメント [ *i* ]: *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="57d95-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="57d95-111">プログラムから、インデックスによって [Comment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="57d95-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="57d95-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="57d95-112">Section index:</span></span>  <br/> |<span data-ttu-id="57d95-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="57d95-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="57d95-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="57d95-114">Row index:</span></span>  <br/> |<span data-ttu-id="57d95-115">**visRowAnnotation** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="57d95-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="57d95-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="57d95-116">Cell index:</span></span>  <br/> |<span data-ttu-id="57d95-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="57d95-117">**visAnnotationComment**</span></span> <br/> |
   

