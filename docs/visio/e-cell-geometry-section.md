---
title: '[E] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: NURBS (nonuniform rational B-spline) の数式が格納されます。
ms.openlocfilehash: 5c9b3cbf96e2a218a8ed790d3a5615843360c95e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423567"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="cc49f-103">[E] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="cc49f-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="cc49f-104">NURBS (nonuniform rational B-spline) の数式が格納されます。</span><span class="sxs-lookup"><span data-stu-id="cc49f-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc49f-105">注釈</span><span class="sxs-lookup"><span data-stu-id="cc49f-105">Remarks</span></span>

<span data-ttu-id="cc49f-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [E] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cc49f-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc49f-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="cc49f-107">Cell name:</span></span>  <br/> | <span data-ttu-id="cc49f-108">Geometry  *i*  .E  *j*            *ここで、i*  と  *j*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="cc49f-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cc49f-109">プログラムから、インデックスによって [E] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cc49f-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc49f-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc49f-110">Section index:</span></span>  <br/> |<span data-ttu-id="cc49f-111">**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cc49f-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cc49f-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc49f-112">Row index:</span></span>  <br/> |<span data-ttu-id="cc49f-113">**visRowVertex**  +  *j* は *j* = 0、1、2..です。</span><span class="sxs-lookup"><span data-stu-id="cc49f-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cc49f-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc49f-114">Cell index:</span></span>  <br/> |<span data-ttu-id="cc49f-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="cc49f-115">**visNURBSData**</span></span> <br/> |
   

