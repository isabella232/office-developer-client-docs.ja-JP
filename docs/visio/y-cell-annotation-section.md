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
description: Y のページ座標内のコメント マーカーの座標です。
ms.openlocfilehash: cc2399de7919512796a39ca39c705c214f4c51a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806825"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="7ec1d-103">[Y] セル ([注釈] セクション)</span><span class="sxs-lookup"><span data-stu-id="7ec1d-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="7ec1d-104">*Y*のページ座標内のコメント マーカーの座標です。</span><span class="sxs-lookup"><span data-stu-id="7ec1d-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7ec1d-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くときにのみ、または .vsd ファイルの形式で .vsdx ファイルを保存するときにコメントを追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ec1d-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="7ec1d-106">Visio 2013 で .vsdx のドキュメント内のコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="7ec1d-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7ec1d-107">注釈</span><span class="sxs-lookup"><span data-stu-id="7ec1d-107">Remarks</span></span>

<span data-ttu-id="7ec1d-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7ec1d-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ec1d-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="7ec1d-109">Cell name:</span></span>  <br/> | <span data-ttu-id="7ec1d-110">Annotation.Y [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="7ec1d-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7ec1d-111">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7ec1d-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ec1d-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7ec1d-112">Section index:</span></span>  <br/> |<span data-ttu-id="7ec1d-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="7ec1d-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="7ec1d-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7ec1d-114">Row index:</span></span>  <br/> |<span data-ttu-id="7ec1d-115">**visRowAnnotation** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="7ec1d-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7ec1d-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7ec1d-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7ec1d-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="7ec1d-117">**visAnnotationY**</span></span> <br/> |
   

