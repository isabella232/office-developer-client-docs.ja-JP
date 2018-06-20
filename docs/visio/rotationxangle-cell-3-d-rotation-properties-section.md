---
title: '[RotationXAngle] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d1a45d32-117a-48e8-ad65-b2723826c3b9
description: 度単位で、x 軸方向の回転の角度を設定 (0.0 から 359.9)。
ms.openlocfilehash: 5992a6e40ab0f956c9aef20b739cdf8bf86dee62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806255"
---
# <a name="rotationxangle-cell-3-d-rotation-properties-section"></a><span data-ttu-id="d8d36-103">[RotationXAngle] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="d8d36-103">RotationXAngle Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="d8d36-104">度単位で、x 軸方向の回転の角度を設定 (0.0 から 359.9)。</span><span class="sxs-lookup"><span data-stu-id="d8d36-104">Determines the angle of rotation along the X-axis, in degrees (0.0 - 359.9).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d8d36-105">備考</span><span class="sxs-lookup"><span data-stu-id="d8d36-105">Remarks</span></span>

<span data-ttu-id="d8d36-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **RotationXAngle** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d8d36-106">To get a reference to the **RotationXAngle** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8d36-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="d8d36-107">Cell name:</span></span>  <br/> |<span data-ttu-id="d8d36-108">RotationXAngle</span><span class="sxs-lookup"><span data-stu-id="d8d36-108">RotationXAngle</span></span>  <br/> |
   
<span data-ttu-id="d8d36-109">プログラムから、インデックスによって [ **RotationXAngle** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d8d36-109">To get a reference to the **RotationXAngle** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8d36-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d8d36-110">Section index:</span></span>  <br/> |<span data-ttu-id="d8d36-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d8d36-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d8d36-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d8d36-112">Row index:</span></span>  <br/> |<span data-ttu-id="d8d36-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="d8d36-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="d8d36-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d8d36-114">Cell index:</span></span>  <br/> |<span data-ttu-id="d8d36-115">**visRotationXAngle**</span><span class="sxs-lookup"><span data-stu-id="d8d36-115">**visRotationXAngle**</span></span> <br/> |
   

