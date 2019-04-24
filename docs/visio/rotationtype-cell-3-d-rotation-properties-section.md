---
title: '[RotationType] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: 図形が並行回転、視点回転、または斜め回転に従って回転するかどうかを、0 から 6 までの整数で決定します。
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315674"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="0082b-103">[RotationType] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="0082b-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="0082b-104">図形が並行回転、視点回転、または斜め回転に従って回転するかどうかを、0 から 6 までの整数で決定します。</span><span class="sxs-lookup"><span data-stu-id="0082b-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="0082b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="0082b-105">**Value**</span></span>|<span data-ttu-id="0082b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="0082b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0082b-107">.0</span><span class="sxs-lookup"><span data-stu-id="0082b-107">0</span></span>  <br/> |<span data-ttu-id="0082b-108">図形に回転は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0082b-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="0082b-109">1-d</span><span class="sxs-lookup"><span data-stu-id="0082b-109">1</span></span>  <br/> |<span data-ttu-id="0082b-110">図形に並行回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="0082b-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="0082b-111">pbm-2</span><span class="sxs-lookup"><span data-stu-id="0082b-111">2</span></span>  <br/> |<span data-ttu-id="0082b-112">図形に視点回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="0082b-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="0082b-113">1/3</span><span class="sxs-lookup"><span data-stu-id="0082b-113">3</span></span>  <br/> |<span data-ttu-id="0082b-114">図形に左上の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="0082b-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="0082b-115">2/4</span><span class="sxs-lookup"><span data-stu-id="0082b-115">4</span></span>  <br/> |<span data-ttu-id="0082b-116">図形に右上の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="0082b-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="0082b-117">5</span><span class="sxs-lookup"><span data-stu-id="0082b-117">5</span></span>  <br/> |<span data-ttu-id="0082b-118">図形に左下の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="0082b-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="0082b-119">シックス</span><span class="sxs-lookup"><span data-stu-id="0082b-119">6</span></span>  <br/> |<span data-ttu-id="0082b-120">図形に右下の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="0082b-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0082b-121">解説</span><span class="sxs-lookup"><span data-stu-id="0082b-121">Remarks</span></span>

<span data-ttu-id="0082b-122">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**RotationType**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0082b-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0082b-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="0082b-123">Cell name:</span></span>  <br/> |<span data-ttu-id="0082b-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="0082b-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="0082b-125">プログラムから、インデックスによって [**RotationType**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0082b-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0082b-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0082b-126">Section index:</span></span>  <br/> |<span data-ttu-id="0082b-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0082b-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0082b-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0082b-128">Row index:</span></span>  <br/> |<span data-ttu-id="0082b-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="0082b-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="0082b-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0082b-130">Cell index:</span></span>  <br/> |<span data-ttu-id="0082b-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="0082b-131">**visRotationType**</span></span> <br/> |
   

