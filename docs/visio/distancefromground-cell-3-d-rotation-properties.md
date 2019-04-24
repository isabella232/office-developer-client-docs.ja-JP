---
title: '[DistanceFromGround] セル ([3-D 回転のプロパティ)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87499dab-977a-45bc-9f6a-8daa80a82abb
description: 3-d で回転したときに、オブジェクトが地上からポイント単位で発生する距離を指定します。
ms.openlocfilehash: aa2f1629ecad234d85d4393411bd40215a671e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332698"
---
# <a name="distancefromground-cell-3-d-rotation-properties"></a><span data-ttu-id="86d94-103">[DistanceFromGround] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="86d94-103">DistanceFromGround Cell (3-D Rotation Properties)</span></span>

<span data-ttu-id="86d94-104">3-d で回転したときに、オブジェクトが地上からポイント単位で発生する距離を指定します。</span><span class="sxs-lookup"><span data-stu-id="86d94-104">Determines the distance the object is raised from the ground in points when rotated in 3-D.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86d94-105">解説</span><span class="sxs-lookup"><span data-stu-id="86d94-105">Remarks</span></span>

<span data-ttu-id="86d94-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[distancefromground]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="86d94-106">To get a reference to the **DistanceFromGround** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86d94-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="86d94-107">Cell name:</span></span>  <br/> |<span data-ttu-id="86d94-108">[distancefromground]</span><span class="sxs-lookup"><span data-stu-id="86d94-108">DistanceFromGround</span></span>  <br/> |
   
<span data-ttu-id="86d94-109">プログラムから、インデックスによって [ **[distancefromground]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="86d94-109">To get a reference to the **DistanceFromGround** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86d94-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="86d94-110">Section index:</span></span>  <br/> |<span data-ttu-id="86d94-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="86d94-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="86d94-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="86d94-112">Row index:</span></span>  <br/> |<span data-ttu-id="86d94-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="86d94-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="86d94-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="86d94-114">Cell index:</span></span>  <br/> |<span data-ttu-id="86d94-115">**visDistanceFromGround**</span><span class="sxs-lookup"><span data-stu-id="86d94-115">**visDistanceFromGround**</span></span> <br/> |
   

