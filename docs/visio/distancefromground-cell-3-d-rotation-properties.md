---
title: '[DistanceFromGround] セル ([3-D 回転のプロパティ)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87499dab-977a-45bc-9f6a-8daa80a82abb
description: オブジェクトに 3-D の回転時に地面から発生する距離を指定します。
ms.openlocfilehash: da544d0340c0fca0103c147f27b715784643153f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805216"
---
# <a name="distancefromground-cell-3-d-rotation-properties"></a><span data-ttu-id="bb6da-103">[DistanceFromGround] セル ([3-D 回転のプロパティ)</span><span class="sxs-lookup"><span data-stu-id="bb6da-103">DistanceFromGround Cell (3-D Rotation Properties)</span></span>

<span data-ttu-id="bb6da-104">オブジェクトに 3-D の回転時に地面から発生する距離を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb6da-104">Determines the distance the object is raised from the ground in points when rotated in 3-D.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb6da-105">備考</span><span class="sxs-lookup"><span data-stu-id="bb6da-105">Remarks</span></span>

<span data-ttu-id="bb6da-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **DistanceFromGround** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="bb6da-106">To get a reference to the **DistanceFromGround** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb6da-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="bb6da-107">Cell name:</span></span>  <br/> |<span data-ttu-id="bb6da-108">DistanceFromGround</span><span class="sxs-lookup"><span data-stu-id="bb6da-108">DistanceFromGround</span></span>  <br/> |
   
<span data-ttu-id="bb6da-109">プログラムから、インデックスによって [ **DistanceFromGround** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="bb6da-109">To get a reference to the **DistanceFromGround** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb6da-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bb6da-110">Section index:</span></span>  <br/> |<span data-ttu-id="bb6da-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bb6da-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bb6da-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bb6da-112">Row index:</span></span>  <br/> |<span data-ttu-id="bb6da-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="bb6da-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="bb6da-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bb6da-114">Cell index:</span></span>  <br/> |<span data-ttu-id="bb6da-115">**visDistanceFromGround**</span><span class="sxs-lookup"><span data-stu-id="bb6da-115">**visDistanceFromGround**</span></span> <br/> |
   

