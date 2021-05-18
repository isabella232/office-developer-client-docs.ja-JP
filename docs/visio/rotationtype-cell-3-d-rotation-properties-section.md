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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422944"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="4ecef-103">[RotationType] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="4ecef-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="4ecef-104">図形が並行回転、視点回転、または斜め回転に従って回転するかどうかを、0 から 6 までの整数で決定します。</span><span class="sxs-lookup"><span data-stu-id="4ecef-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="4ecef-105">**値**</span><span class="sxs-lookup"><span data-stu-id="4ecef-105">**Value**</span></span>|<span data-ttu-id="4ecef-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="4ecef-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ecef-107">0</span><span class="sxs-lookup"><span data-stu-id="4ecef-107">0</span></span>  <br/> |<span data-ttu-id="4ecef-108">図形に回転は適用されません。</span><span class="sxs-lookup"><span data-stu-id="4ecef-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="4ecef-109">1</span><span class="sxs-lookup"><span data-stu-id="4ecef-109">1</span></span>  <br/> |<span data-ttu-id="4ecef-110">図形に並行回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ecef-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="4ecef-111">2</span><span class="sxs-lookup"><span data-stu-id="4ecef-111">2</span></span>  <br/> |<span data-ttu-id="4ecef-112">図形に視点回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ecef-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="4ecef-113">3</span><span class="sxs-lookup"><span data-stu-id="4ecef-113">3</span></span>  <br/> |<span data-ttu-id="4ecef-114">図形に左上の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ecef-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="4ecef-115">4</span><span class="sxs-lookup"><span data-stu-id="4ecef-115">4</span></span>  <br/> |<span data-ttu-id="4ecef-116">図形に右上の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ecef-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="4ecef-117">5</span><span class="sxs-lookup"><span data-stu-id="4ecef-117">5</span></span>  <br/> |<span data-ttu-id="4ecef-118">図形に左下の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ecef-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="4ecef-119">6</span><span class="sxs-lookup"><span data-stu-id="4ecef-119">6</span></span>  <br/> |<span data-ttu-id="4ecef-120">図形に右下の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ecef-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ecef-121">注釈</span><span class="sxs-lookup"><span data-stu-id="4ecef-121">Remarks</span></span>

<span data-ttu-id="4ecef-122">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**RotationType**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4ecef-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ecef-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="4ecef-123">Cell name:</span></span>  <br/> |<span data-ttu-id="4ecef-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="4ecef-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="4ecef-125">プログラムから、インデックスによって [**RotationType**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ecef-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ecef-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4ecef-126">Section index:</span></span>  <br/> |<span data-ttu-id="4ecef-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4ecef-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4ecef-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4ecef-128">Row index:</span></span>  <br/> |<span data-ttu-id="4ecef-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="4ecef-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="4ecef-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4ecef-130">Cell index:</span></span>  <br/> |<span data-ttu-id="4ecef-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="4ecef-131">**visRotationType**</span></span> <br/> |
   

