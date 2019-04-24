---
title: '[ReplaceLockShapeData] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。 ReplaceLockShapeData は、マスター シェイプの図形データが、置換される図形の図形データすべてに優先するかどうかを決定します。
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348343"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="55870-104">[ReplaceLockShapeData] セル ([図形の動作の変更] セクション)</span><span class="sxs-lookup"><span data-stu-id="55870-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="55870-105">マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="55870-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="55870-106">**ReplaceLockShapeData** は、マスター シェイプの図形データが、置換される図形の図形データすべてに優先するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="55870-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="55870-107">**値**</span><span class="sxs-lookup"><span data-stu-id="55870-107">**Value**</span></span>|<span data-ttu-id="55870-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="55870-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55870-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="55870-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="55870-110">マスター シェイプの [**Shape Data**] セクションにあるすべての行と値は、置換後の図形にコピーされ、置換される古い図形のローカル値はすべて破棄されます。</span><span class="sxs-lookup"><span data-stu-id="55870-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="55870-111">0 (FALSE)</span><span class="sxs-lookup"><span data-stu-id="55870-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="55870-p103">マスター シェイプの [**図形データ**] セクションの行と値は、置換される図形にコピーされます。ローカル値を使用した古い図形の [**図形データ**] セクションの行は、置換後の図形に転送されます。</span><span class="sxs-lookup"><span data-stu-id="55870-p103">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape. Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="55870-114">解説</span><span class="sxs-lookup"><span data-stu-id="55870-114">Remarks</span></span>

<span data-ttu-id="55870-115">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ReplaceLockShapeData**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="55870-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55870-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="55870-116">Cell name:</span></span>  <br/> | <span data-ttu-id="55870-117">[replacelockshapedata]</span><span class="sxs-lookup"><span data-stu-id="55870-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="55870-118">プログラムから、インデックスによって [**ReplaceLockShapeData**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="55870-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55870-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="55870-119">Section index:</span></span>  <br/> |<span data-ttu-id="55870-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="55870-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="55870-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="55870-121">Row index:</span></span>  <br/> |<span data-ttu-id="55870-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="55870-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="55870-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="55870-123">Cell index:</span></span>  <br/> |<span data-ttu-id="55870-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="55870-124">**visReplaceLockShapeData**</span></span> <br/> |
   

