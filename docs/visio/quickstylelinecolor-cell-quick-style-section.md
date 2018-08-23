---
title: '[QuickStyleLineColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: 0 ~ 7 の整数として、図形の線を使用するテーマの色を決定します。
ms.openlocfilehash: 2a660472998ade8148e8b70a3c6e4fc5fb3f4820
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806153"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a><span data-ttu-id="d188c-103">[QuickStyleLineColor] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="d188c-103">QuickStyleLineColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="d188c-104">0 ~ 7 の整数として、図形の線を使用するテーマの色を決定します。</span><span class="sxs-lookup"><span data-stu-id="d188c-104">Determines which theme color that a shape's line uses, as an integer from 0 to 7.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d188c-105">値</span><span class="sxs-lookup"><span data-stu-id="d188c-105">Value</span></span>  <br/> |<span data-ttu-id="d188c-106">説明</span><span class="sxs-lookup"><span data-stu-id="d188c-106">Description</span></span>  <br/> |
|<span data-ttu-id="d188c-107">0</span><span class="sxs-lookup"><span data-stu-id="d188c-107">0</span></span>  <br/> |<span data-ttu-id="d188c-108">図形の線の色は、[ダーク] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="d188c-108">The shape line color inherits from the Dark theme color.</span></span>  <br/> |
|<span data-ttu-id="d188c-109">1</span><span class="sxs-lookup"><span data-stu-id="d188c-109">1</span></span>  <br/> |<span data-ttu-id="d188c-110">図形の線の色は、[ライト] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="d188c-110">The shape line color inherits from the Light theme color.</span></span>  <br/> |
|<span data-ttu-id="d188c-111">2</span><span class="sxs-lookup"><span data-stu-id="d188c-111">2</span></span>  <br/> |<span data-ttu-id="d188c-112">図形の線の色は、[アクセント 1] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="d188c-112">The shape line color inherits from the Accent 1 theme color</span></span>  <br/> |
|<span data-ttu-id="d188c-113">3</span><span class="sxs-lookup"><span data-stu-id="d188c-113">3</span></span>  <br/> |<span data-ttu-id="d188c-114">図形の線の色は、[アクセント 2] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="d188c-114">The shape line color inherits from the Accent 2 theme color</span></span>  <br/> |
|<span data-ttu-id="d188c-115">4</span><span class="sxs-lookup"><span data-stu-id="d188c-115">4</span></span>  <br/> |<span data-ttu-id="d188c-116">図形の線の色は、[アクセント 3] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="d188c-116">The shape line color inherits from the Accent 3 theme color</span></span>  <br/> |
|<span data-ttu-id="d188c-117">5</span><span class="sxs-lookup"><span data-stu-id="d188c-117">5</span></span>  <br/> |<span data-ttu-id="d188c-118">図形の線の色は、[アクセント 4] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="d188c-118">The shape line color inherits from the Accent 4 theme color</span></span>  <br/> |
|<span data-ttu-id="d188c-119">6</span><span class="sxs-lookup"><span data-stu-id="d188c-119">6</span></span>  <br/> |<span data-ttu-id="d188c-120">図形の線の色は、[アクセント 5] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="d188c-120">The shape line color inherits from the Accent 5 theme color</span></span>  <br/> |
|<span data-ttu-id="d188c-121">7</span><span class="sxs-lookup"><span data-stu-id="d188c-121">7</span></span>  <br/> |<span data-ttu-id="d188c-122">図形の線の色は、[アクセント 6] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="d188c-122">The shape line color inherits from the Accent 6 theme color</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d188c-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="d188c-123">Remarks</span></span>

<span data-ttu-id="d188c-124">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleLineColor**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d188c-124">To get a reference to the **QuickStyleLineColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d188c-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="d188c-125">Cell name:</span></span>  <br/> | <span data-ttu-id="d188c-126">QuickStyleLineColor</span><span class="sxs-lookup"><span data-stu-id="d188c-126">QuickStyleLineColor</span></span>  <br/> |
   
<span data-ttu-id="d188c-127">プログラムから、インデックスによって [**QuickStyleLineColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d188c-127">To get a reference to the **QuickStyleLineColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d188c-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d188c-128">Section index:</span></span>  <br/> |<span data-ttu-id="d188c-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d188c-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d188c-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d188c-130">Row index:</span></span>  <br/> |<span data-ttu-id="d188c-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="d188c-131">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="d188c-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d188c-132">Cell index:</span></span>  <br/> |<span data-ttu-id="d188c-133">**visQuickStyleLineColor**</span><span class="sxs-lookup"><span data-stu-id="d188c-133">**visQuickStyleLineColor**</span></span> <br/> |
   

