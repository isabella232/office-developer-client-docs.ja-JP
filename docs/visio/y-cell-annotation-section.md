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
description: ページ座標内のコメントマーカーの y 座標です。
ms.openlocfilehash: 48a37c261078cd1000331920b33549cee2c1da03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360124"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="5aaf4-103">[Y] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="5aaf4-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="5aaf4-104">ページ座標内のコメントマーカーの*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="5aaf4-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5aaf4-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くとき、または .vsd ファイル形式で .vsdx ファイルを保存するときにのみ、コメントの追跡に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5aaf4-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="5aaf4-106">これは、Visio 2013 の .vsdx ドキュメントでコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="5aaf4-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5aaf4-107">解説</span><span class="sxs-lookup"><span data-stu-id="5aaf4-107">Remarks</span></span>

<span data-ttu-id="5aaf4-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5aaf4-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5aaf4-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="5aaf4-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5aaf4-110">Annotation. Y [ *i* ] = \*\* <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="5aaf4-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5aaf4-111">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5aaf4-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5aaf4-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5aaf4-112">Section index:</span></span>  <br/> |<span data-ttu-id="5aaf4-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="5aaf4-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="5aaf4-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5aaf4-114">Row index:</span></span>  <br/> |<span data-ttu-id="5aaf4-115">**visRowAnnotation** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="5aaf4-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5aaf4-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5aaf4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5aaf4-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="5aaf4-117">**visAnnotationY**</span></span> <br/> |
   

