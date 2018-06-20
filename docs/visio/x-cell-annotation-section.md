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
description: X ページ座標内のコメント マーカーの座標です。
ms.openlocfilehash: 454c28c6f15c705148155751d533a516aae7d2d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806799"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="5ebc7-103">[X] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="5ebc7-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="5ebc7-104">*X*のページ座標内のコメント マーカーの座標です。</span><span class="sxs-lookup"><span data-stu-id="5ebc7-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5ebc7-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くときにのみ、または .vsd ファイルの形式で .vsdx ファイルを保存するときにコメントを追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ebc7-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="5ebc7-106">Visio 2013 で .vsdx のドキュメント内のコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="5ebc7-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5ebc7-107">備考</span><span class="sxs-lookup"><span data-stu-id="5ebc7-107">Remarks</span></span>

<span data-ttu-id="5ebc7-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="5ebc7-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ebc7-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="5ebc7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5ebc7-110">Annotation.X [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="5ebc7-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5ebc7-111">プログラムから、インデックスによって [X] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5ebc7-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ebc7-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5ebc7-112">Section index:</span></span>  <br/> |<span data-ttu-id="5ebc7-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="5ebc7-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="5ebc7-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5ebc7-114">Row index:</span></span>  <br/> |<span data-ttu-id="5ebc7-115">**visRowAnnotation** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="5ebc7-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5ebc7-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5ebc7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5ebc7-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="5ebc7-117">**visAnnotationX**</span></span> <br/> |
   

