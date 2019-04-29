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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422531"
---
# <a name="perspective-cell-3-d-rotation-properties-section"></a><span data-ttu-id="480a4-103">[Perspective] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="480a4-103">Perspective Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="480a4-104">遠近回転の遠近の角度を指定します。角度は° (0 ~ 359.9) を指定します。</span><span class="sxs-lookup"><span data-stu-id="480a4-104">Determines the perspective angle for a perspective rotation, in degrees (0 to 359.9)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="480a4-105">注釈</span><span class="sxs-lookup"><span data-stu-id="480a4-105">Remarks</span></span>

<span data-ttu-id="480a4-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **Perspective** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="480a4-106">To get a reference to the **Perspective** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="480a4-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="480a4-107">Cell name:</span></span>  <br/> |<span data-ttu-id="480a4-108">Perspective</span><span class="sxs-lookup"><span data-stu-id="480a4-108">Perspective</span></span>  <br/> |
   
<span data-ttu-id="480a4-109">プログラムから、インデックスによって [ **Perspective** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="480a4-109">To get a reference to the **Perspective** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="480a4-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="480a4-110">Section index:</span></span>  <br/> |<span data-ttu-id="480a4-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="480a4-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="480a4-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="480a4-112">Row index:</span></span>  <br/> |<span data-ttu-id="480a4-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="480a4-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="480a4-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="480a4-114">Cell index:</span></span>  <br/> |<span data-ttu-id="480a4-115">**visPerspective**</span><span class="sxs-lookup"><span data-stu-id="480a4-115">**visPerspective**</span></span> <br/> |
   

