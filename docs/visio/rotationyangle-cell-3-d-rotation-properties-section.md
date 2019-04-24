---
title: '[RotationYAngle] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 642d5931-aba3-443d-8c11-d12aa8e56d05
description: Y 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。
ms.openlocfilehash: a0ec330ded88aace6c8e4ab658fceca79eb94570
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315590"
---
# <a name="rotationyangle-cell-3-d-rotation-properties-section"></a><span data-ttu-id="19b96-103">[RotationYAngle] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="19b96-103">RotationYAngle Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="19b96-104">Y 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。</span><span class="sxs-lookup"><span data-stu-id="19b96-104">Determines the angle of rotation along the Y-axis, in degrees (0.0 - 359.9).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19b96-105">解説</span><span class="sxs-lookup"><span data-stu-id="19b96-105">Remarks</span></span>

<span data-ttu-id="19b96-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[rotationyangle]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="19b96-106">To get a reference to the **RotationYAngle** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19b96-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="19b96-107">Cell name:</span></span>  <br/> |<span data-ttu-id="19b96-108">[rotationyangle]</span><span class="sxs-lookup"><span data-stu-id="19b96-108">RotationYAngle</span></span>  <br/> |
   
<span data-ttu-id="19b96-109">プログラムから、インデックスによって [ **[rotationyangle]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="19b96-109">To get a reference to the **RotationYAngle** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19b96-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="19b96-110">Section index:</span></span>  <br/> |<span data-ttu-id="19b96-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="19b96-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="19b96-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="19b96-112">Row index:</span></span>  <br/> |<span data-ttu-id="19b96-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="19b96-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="19b96-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="19b96-114">Cell index:</span></span>  <br/> |<span data-ttu-id="19b96-115">**visRotationYAngle**</span><span class="sxs-lookup"><span data-stu-id="19b96-115">**visRotationYAngle**</span></span> <br/> |
   

