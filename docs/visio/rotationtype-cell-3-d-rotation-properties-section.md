---
title: '[RotationType] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: 図形が並行回転、視点回転、または斜め回転に従って回転するかどうかを、0 から 6 までの整数で決定します。
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806286"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="044ee-103">[RotationType] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="044ee-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="044ee-104">図形が並行回転、視点回転、または斜め回転に従って回転するかどうかを、0 から 6 までの整数で決定します。</span><span class="sxs-lookup"><span data-stu-id="044ee-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="044ee-105">**値**</span><span class="sxs-lookup"><span data-stu-id="044ee-105">**Value**</span></span>|<span data-ttu-id="044ee-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="044ee-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="044ee-107">0</span><span class="sxs-lookup"><span data-stu-id="044ee-107">0</span></span>  <br/> |<span data-ttu-id="044ee-108">図形に回転は適用されません。</span><span class="sxs-lookup"><span data-stu-id="044ee-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="044ee-109">1</span><span class="sxs-lookup"><span data-stu-id="044ee-109">1</span></span>  <br/> |<span data-ttu-id="044ee-110">図形に並行回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="044ee-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="044ee-111">2</span><span class="sxs-lookup"><span data-stu-id="044ee-111">2</span></span>  <br/> |<span data-ttu-id="044ee-112">図形に視点回転が適用されます。 </span><span class="sxs-lookup"><span data-stu-id="044ee-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="044ee-113">3</span><span class="sxs-lookup"><span data-stu-id="044ee-113">3</span></span>  <br/> |<span data-ttu-id="044ee-114">図形に左上の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="044ee-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="044ee-115">4</span><span class="sxs-lookup"><span data-stu-id="044ee-115">4</span></span>  <br/> |<span data-ttu-id="044ee-116">図形に右上の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="044ee-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="044ee-117">5</span><span class="sxs-lookup"><span data-stu-id="044ee-117">5</span></span>  <br/> |<span data-ttu-id="044ee-118">図形に左下の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="044ee-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="044ee-119">6</span><span class="sxs-lookup"><span data-stu-id="044ee-119">6</span></span>  <br/> |<span data-ttu-id="044ee-120">図形に右下の斜め回転が適用されます。</span><span class="sxs-lookup"><span data-stu-id="044ee-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="044ee-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="044ee-121">Remarks</span></span>

<span data-ttu-id="044ee-122">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**RotationType**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="044ee-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="044ee-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="044ee-123">Cell name:</span></span>  <br/> |<span data-ttu-id="044ee-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="044ee-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="044ee-125">プログラムから、インデックスによって [**RotationType**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="044ee-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="044ee-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="044ee-126">Section index:</span></span>  <br/> |<span data-ttu-id="044ee-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="044ee-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="044ee-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="044ee-128">Row index:</span></span>  <br/> |<span data-ttu-id="044ee-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="044ee-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="044ee-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="044ee-130">Cell index:</span></span>  <br/> |<span data-ttu-id="044ee-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="044ee-131">**visRotationType**</span></span> <br/> |
   

