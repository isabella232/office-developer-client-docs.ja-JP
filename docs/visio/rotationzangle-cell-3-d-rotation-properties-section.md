---
title: '[RotationZAngle] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c39b7f7-1cd7-4e0d-946c-356705194583
description: Z 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。
ms.openlocfilehash: 8cabf6995b523cdbd91e7ac54085ad02a2521191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315562"
---
# <a name="rotationzangle-cell-3-d-rotation-properties-section"></a><span data-ttu-id="bed4f-103">[RotationZAngle] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="bed4f-103">RotationZAngle Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="bed4f-104">Z 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。</span><span class="sxs-lookup"><span data-stu-id="bed4f-104">Determines the angle of rotation along the Z-axis, in degrees (0.0 - 359.9).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bed4f-105">解説</span><span class="sxs-lookup"><span data-stu-id="bed4f-105">Remarks</span></span>

<span data-ttu-id="bed4f-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[rotationzangle]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bed4f-106">To get a reference to the **RotationZAngle** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bed4f-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="bed4f-107">Cell name:</span></span>  <br/> |<span data-ttu-id="bed4f-108">[rotationzangle]</span><span class="sxs-lookup"><span data-stu-id="bed4f-108">RotationZAngle</span></span>  <br/> |
   
<span data-ttu-id="bed4f-109">プログラムから、インデックスによって [ **[rotationzangle]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bed4f-109">To get a reference to the **RotationZAngle** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bed4f-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bed4f-110">Section index:</span></span>  <br/> |<span data-ttu-id="bed4f-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bed4f-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bed4f-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bed4f-112">Row index:</span></span>  <br/> |<span data-ttu-id="bed4f-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="bed4f-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="bed4f-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bed4f-114">Cell index:</span></span>  <br/> |<span data-ttu-id="bed4f-115">**visRotationZAngle**</span><span class="sxs-lookup"><span data-stu-id="bed4f-115">**visRotationZAngle**</span></span> <br/> |
   

