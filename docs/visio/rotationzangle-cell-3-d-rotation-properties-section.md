---
title: '[RotationZAngle] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c39b7f7-1cd7-4e0d-946c-356705194583
description: 度で、z 軸に沿った回転の角度を設定 (0.0 から 359.9)。
ms.openlocfilehash: c0a3ab4eec54ec6cf1f534eef1a620a1b5ea2c11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806267"
---
# <a name="rotationzangle-cell-3-d-rotation-properties-section"></a><span data-ttu-id="31ced-103">[RotationZAngle] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="31ced-103">RotationZAngle Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="31ced-104">度で、z 軸に沿った回転の角度を設定 (0.0 から 359.9)。</span><span class="sxs-lookup"><span data-stu-id="31ced-104">Determines the angle of rotation along the Z-axis, in degrees (0.0 - 359.9).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31ced-105">備考</span><span class="sxs-lookup"><span data-stu-id="31ced-105">Remarks</span></span>

<span data-ttu-id="31ced-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **RotationZAngle** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="31ced-106">To get a reference to the **RotationZAngle** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31ced-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="31ced-107">Cell name:</span></span>  <br/> |<span data-ttu-id="31ced-108">RotationZAngle</span><span class="sxs-lookup"><span data-stu-id="31ced-108">RotationZAngle</span></span>  <br/> |
   
<span data-ttu-id="31ced-109">プログラムから、インデックスによって [ **RotationZAngle** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="31ced-109">To get a reference to the **RotationZAngle** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31ced-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="31ced-110">Section index:</span></span>  <br/> |<span data-ttu-id="31ced-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="31ced-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="31ced-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="31ced-112">Row index:</span></span>  <br/> |<span data-ttu-id="31ced-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="31ced-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="31ced-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="31ced-114">Cell index:</span></span>  <br/> |<span data-ttu-id="31ced-115">**visRotationZAngle**</span><span class="sxs-lookup"><span data-stu-id="31ced-115">**visRotationZAngle**</span></span> <br/> |
   

