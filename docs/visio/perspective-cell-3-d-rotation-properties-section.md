---
title: '[Perspective] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e07d97a4-9896-4b88-9e76-5a1b3f133094
description: 遠近回転の遠近の角度を指定します。角度は° (0 ~ 359.9) を指定します。
ms.openlocfilehash: 4cbefc2fa147a418fa792542e1dc57c39ab2490c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307771"
---
# <a name="perspective-cell-3-d-rotation-properties-section"></a><span data-ttu-id="eff5b-103">[Perspective] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="eff5b-103">Perspective Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="eff5b-104">遠近回転の遠近の角度を指定します。角度は° (0 ~ 359.9) を指定します。</span><span class="sxs-lookup"><span data-stu-id="eff5b-104">Determines the perspective angle for a perspective rotation, in degrees (0 to 359.9)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eff5b-105">解説</span><span class="sxs-lookup"><span data-stu-id="eff5b-105">Remarks</span></span>

<span data-ttu-id="eff5b-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **Perspective** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="eff5b-106">To get a reference to the **Perspective** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eff5b-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="eff5b-107">Cell name:</span></span>  <br/> |<span data-ttu-id="eff5b-108">Perspective</span><span class="sxs-lookup"><span data-stu-id="eff5b-108">Perspective</span></span>  <br/> |
   
<span data-ttu-id="eff5b-109">プログラムから、インデックスによって [ **Perspective** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eff5b-109">To get a reference to the **Perspective** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eff5b-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eff5b-110">Section index:</span></span>  <br/> |<span data-ttu-id="eff5b-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eff5b-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="eff5b-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="eff5b-112">Row index:</span></span>  <br/> |<span data-ttu-id="eff5b-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="eff5b-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="eff5b-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eff5b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="eff5b-115">**visPerspective**</span><span class="sxs-lookup"><span data-stu-id="eff5b-115">**visPerspective**</span></span> <br/> |
   

