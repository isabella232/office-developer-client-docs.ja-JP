---
title: '[Y] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: ページ座標のコメント マーカーの y 座標。
ms.openlocfilehash: 48a37c261078cd1000331920b33549cee2c1da03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429202"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="34846-103">[Y] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="34846-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="34846-104">ページ  *座標の*  コメント マーカーの y 座標。</span><span class="sxs-lookup"><span data-stu-id="34846-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="34846-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開く場合、または .vsd ファイル形式で .vsdx ファイルを保存する場合にのみ、コメントを追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="34846-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="34846-106">2013 年の .vsdx ドキュメントのコメントを追跡Visioされません。</span><span class="sxs-lookup"><span data-stu-id="34846-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="34846-107">注釈</span><span class="sxs-lookup"><span data-stu-id="34846-107">Remarks</span></span>

<span data-ttu-id="34846-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="34846-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34846-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="34846-109">Cell name:</span></span>  <br/> | <span data-ttu-id="34846-110">Annotation.Y [  *i*  ] ここで  *、i*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="34846-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="34846-111">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="34846-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34846-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="34846-112">Section index:</span></span>  <br/> |<span data-ttu-id="34846-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="34846-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="34846-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="34846-114">Row index:</span></span>  <br/> |<span data-ttu-id="34846-115">**visRowAnnotation**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="34846-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="34846-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="34846-116">Cell index:</span></span>  <br/> |<span data-ttu-id="34846-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="34846-117">**visAnnotationY**</span></span> <br/> |
   

