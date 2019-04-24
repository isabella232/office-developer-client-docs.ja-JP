---
title: '[X] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: ページ座標内のコメントマーカーの x 座標です。
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341309"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="a4729-103">[X] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="a4729-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="a4729-104">ページ座標内のコメントマーカーの*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="a4729-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a4729-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くとき、または .vsd ファイル形式で .vsdx ファイルを保存するときにのみ、コメントの追跡に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4729-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="a4729-106">これは、Visio 2013 の .vsdx ドキュメントでコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="a4729-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a4729-107">解説</span><span class="sxs-lookup"><span data-stu-id="a4729-107">Remarks</span></span>

<span data-ttu-id="a4729-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a4729-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a4729-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="a4729-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a4729-110"><1> [ *i* ]: *i* =、2、3...</span><span class="sxs-lookup"><span data-stu-id="a4729-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a4729-111">プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4729-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a4729-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a4729-112">Section index:</span></span>  <br/> |<span data-ttu-id="a4729-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="a4729-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="a4729-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a4729-114">Row index:</span></span>  <br/> |<span data-ttu-id="a4729-115">**visRowAnnotation** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="a4729-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a4729-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a4729-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a4729-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="a4729-117">**visAnnotationX**</span></span> <br/> |
   

