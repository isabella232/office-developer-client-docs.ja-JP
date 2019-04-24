---
title: '[NoQuickDrag] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: ユーザーが [Geometry] セクションで定義された塗りつぶされた領域をクリックしたときに、図形を選択またはドラッグできるかどうかを指定します。
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341063"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="6267f-103">[NoQuickDrag] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="6267f-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="6267f-104">ユーザーが [Geometry] セクションで定義された塗りつぶされた領域をクリックしたときに、図形を選択またはドラッグできるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6267f-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6267f-105">解説</span><span class="sxs-lookup"><span data-stu-id="6267f-105">Remarks</span></span>

<span data-ttu-id="6267f-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoQuickDrag] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6267f-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6267f-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="6267f-107">Cell name:</span></span>  <br/> |<span data-ttu-id="6267f-108">ジオメトリ*i*noquickdrag、where \* i \*-<1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="6267f-108">Geometry  *i*  .NoQuickDrag, where  \* i \*  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6267f-109">プログラムから、インデックスによって [NoQuickDrag] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6267f-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6267f-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6267f-110">Section index:</span></span>  <br/> |<span data-ttu-id="6267f-111">**visSectionFirstComponent** +  *i* 、 *i* = 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="6267f-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6267f-112">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="6267f-112">Row index:</span></span>  <br/> |<span data-ttu-id="6267f-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="6267f-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="6267f-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6267f-114">Cell index:</span></span>  <br/> |<span data-ttu-id="6267f-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="6267f-115">**visCompNoQuickDrag**</span></span> <br/> |
   

