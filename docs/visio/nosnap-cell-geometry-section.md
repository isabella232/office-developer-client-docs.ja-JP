---
title: '[NoSnap] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: 他の図形がパスにスナップされるかどうかを指定します。
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341133"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="eb966-103">[NoSnap] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="eb966-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="eb966-104">他の図形がパスにスナップされるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="eb966-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="eb966-105">**値**</span><span class="sxs-lookup"><span data-stu-id="eb966-105">**Value**</span></span>|<span data-ttu-id="eb966-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="eb966-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="eb966-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="eb966-107">TRUE</span></span>  <br/> | <span data-ttu-id="eb966-108">他の図形はこのパスにスナップできません。</span><span class="sxs-lookup"><span data-stu-id="eb966-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="eb966-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="eb966-109">FALSE</span></span>  <br/> | <span data-ttu-id="eb966-110">他の図形はこのパスにスナップできます。</span><span class="sxs-lookup"><span data-stu-id="eb966-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb966-111">解説</span><span class="sxs-lookup"><span data-stu-id="eb966-111">Remarks</span></span>

<span data-ttu-id="eb966-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoSnap] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb966-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb966-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="eb966-113">Cell name:</span></span>  <br/> | <span data-ttu-id="eb966-114">ジオメトリ*i*[nosnap] where *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="eb966-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="eb966-115">プログラムから、インデックスによって [NoSnap] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eb966-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb966-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb966-116">Section index:</span></span>  <br/> |<span data-ttu-id="eb966-117">**visSectionFirstComponent** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="eb966-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="eb966-118">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="eb966-118">Row index:</span></span>  <br/> |<span data-ttu-id="eb966-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="eb966-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="eb966-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb966-120">Cell index:</span></span>  <br/> |<span data-ttu-id="eb966-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="eb966-121">**visCompNoSnap**</span></span> <br/> |
   

