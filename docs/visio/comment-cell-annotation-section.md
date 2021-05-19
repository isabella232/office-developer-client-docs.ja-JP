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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415531"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="11dc1-103">[Comment] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="11dc1-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="11dc1-104">コメント内に表示されるテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="11dc1-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="11dc1-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開く場合、または .vsd ファイル形式で .vsdx ファイルを保存する場合にのみ、コメントを追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="11dc1-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="11dc1-106">2013 年の .vsdx ドキュメントのコメントを追跡Visioされません。</span><span class="sxs-lookup"><span data-stu-id="11dc1-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="11dc1-107">注釈</span><span class="sxs-lookup"><span data-stu-id="11dc1-107">Remarks</span></span>

<span data-ttu-id="11dc1-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Comment] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="11dc1-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11dc1-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="11dc1-109">Cell name:</span></span>  <br/> | <span data-ttu-id="11dc1-110">Annotation.Comment[  *i*  ]  *ここで、i*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="11dc1-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="11dc1-111">プログラムから、インデックスによって [Comment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="11dc1-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11dc1-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="11dc1-112">Section index:</span></span>  <br/> |<span data-ttu-id="11dc1-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="11dc1-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="11dc1-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="11dc1-114">Row index:</span></span>  <br/> |<span data-ttu-id="11dc1-115">**visRowAnnotation**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="11dc1-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="11dc1-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="11dc1-116">Cell index:</span></span>  <br/> |<span data-ttu-id="11dc1-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="11dc1-117">**visAnnotationComment**</span></span> <br/> |
   

