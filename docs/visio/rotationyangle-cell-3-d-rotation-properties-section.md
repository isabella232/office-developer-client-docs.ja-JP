---
title: '[RotationYAngle] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 642d5931-aba3-443d-8c11-d12aa8e56d05
description: 度単位で、y 軸方向の回転の角度を設定 (0.0 から 359.9)。
ms.openlocfilehash: 4691b856f35e74a700030a54685831d6e4acdff4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806257"
---
# <a name="rotationyangle-cell-3-d-rotation-properties-section"></a><span data-ttu-id="fbe4c-103">[RotationYAngle] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="fbe4c-103">RotationYAngle Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="fbe4c-104">度単位で、y 軸方向の回転の角度を設定 (0.0 から 359.9)。</span><span class="sxs-lookup"><span data-stu-id="fbe4c-104">Determines the angle of rotation along the Y-axis, in degrees (0.0 - 359.9).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbe4c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="fbe4c-105">Remarks</span></span>

<span data-ttu-id="fbe4c-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **RotationYAngle** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="fbe4c-106">To get a reference to the **RotationYAngle** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbe4c-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="fbe4c-107">Cell name:</span></span>  <br/> |<span data-ttu-id="fbe4c-108">RotationYAngle</span><span class="sxs-lookup"><span data-stu-id="fbe4c-108">RotationYAngle</span></span>  <br/> |
   
<span data-ttu-id="fbe4c-109">プログラムから、インデックスによって [ **RotationYAngle** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="fbe4c-109">To get a reference to the **RotationYAngle** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbe4c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fbe4c-110">Section index:</span></span>  <br/> |<span data-ttu-id="fbe4c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fbe4c-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fbe4c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fbe4c-112">Row index:</span></span>  <br/> |<span data-ttu-id="fbe4c-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="fbe4c-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="fbe4c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fbe4c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="fbe4c-115">**visRotationYAngle**</span><span class="sxs-lookup"><span data-stu-id="fbe4c-115">**visRotationYAngle**</span></span> <br/> |
   

