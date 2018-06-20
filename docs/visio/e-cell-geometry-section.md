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
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805295"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="04e15-103">[E] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="04e15-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="04e15-104">NURBS (nonuniform rational B-spline) の数式が格納されます。</span><span class="sxs-lookup"><span data-stu-id="04e15-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="04e15-105">備考</span><span class="sxs-lookup"><span data-stu-id="04e15-105">Remarks</span></span>

<span data-ttu-id="04e15-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[E] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="04e15-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04e15-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="04e15-107">Cell name:</span></span>  <br/> | <span data-ttu-id="04e15-108">ジオメトリの*i*です。E *j* 、 *i*および*j* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="04e15-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="04e15-109">プログラムから、インデックスによって [E] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="04e15-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04e15-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="04e15-110">Section index:</span></span>  <br/> |<span data-ttu-id="04e15-111">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="04e15-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="04e15-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="04e15-112">Row index:</span></span>  <br/> |<span data-ttu-id="04e15-113">**visRowVertex** +  *j* 、 *j* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="04e15-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="04e15-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="04e15-114">Cell index:</span></span>  <br/> |<span data-ttu-id="04e15-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="04e15-115">**visNURBSData**</span></span> <br/> |
   

