---
title: '[QuickStyleLineColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: 図形の線が使用するテーマの色を、0から7の整数で指定します。
ms.openlocfilehash: 010b943f2266b1e0ee192e5f1341d73851d176fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360050"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a><span data-ttu-id="fdde3-103">[QuickStyleLineColor] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="fdde3-103">QuickStyleLineColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="fdde3-104">図形の線が使用するテーマの色を、0から7の整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="fdde3-104">Determines which theme color that a shape's line uses, as an integer from 0 to 7.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fdde3-105">値</span><span class="sxs-lookup"><span data-stu-id="fdde3-105">Value</span></span>  <br/> |<span data-ttu-id="fdde3-106">説明</span><span class="sxs-lookup"><span data-stu-id="fdde3-106">Description</span></span>  <br/> |
|<span data-ttu-id="fdde3-107">.0</span><span class="sxs-lookup"><span data-stu-id="fdde3-107">0</span></span>  <br/> |<span data-ttu-id="fdde3-108">図形の線の色は、[ダーク] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="fdde3-108">The shape line color inherits from the Dark theme color.</span></span>  <br/> |
|<span data-ttu-id="fdde3-109">1-d</span><span class="sxs-lookup"><span data-stu-id="fdde3-109">1</span></span>  <br/> |<span data-ttu-id="fdde3-110">図形の線の色は、[ライト] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="fdde3-110">The shape line color inherits from the Light theme color.</span></span>  <br/> |
|<span data-ttu-id="fdde3-111">pbm-2</span><span class="sxs-lookup"><span data-stu-id="fdde3-111">2</span></span>  <br/> |<span data-ttu-id="fdde3-112">図形の線の色は、[アクセント 1] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="fdde3-112">The shape line color inherits from the Accent 1 theme color</span></span>  <br/> |
|<span data-ttu-id="fdde3-113">1/3</span><span class="sxs-lookup"><span data-stu-id="fdde3-113">3</span></span>  <br/> |<span data-ttu-id="fdde3-114">図形の線の色は、[アクセント 2] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="fdde3-114">The shape line color inherits from the Accent 2 theme color</span></span>  <br/> |
|<span data-ttu-id="fdde3-115">2/4</span><span class="sxs-lookup"><span data-stu-id="fdde3-115">4</span></span>  <br/> |<span data-ttu-id="fdde3-116">図形の線の色は、[アクセント 3] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="fdde3-116">The shape line color inherits from the Accent 3 theme color</span></span>  <br/> |
|<span data-ttu-id="fdde3-117">5</span><span class="sxs-lookup"><span data-stu-id="fdde3-117">5</span></span>  <br/> |<span data-ttu-id="fdde3-118">図形の線の色は、[アクセント 4] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="fdde3-118">The shape line color inherits from the Accent 4 theme color</span></span>  <br/> |
|<span data-ttu-id="fdde3-119">シックス</span><span class="sxs-lookup"><span data-stu-id="fdde3-119">6</span></span>  <br/> |<span data-ttu-id="fdde3-120">図形の線の色は、[アクセント 5] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="fdde3-120">The shape line color inherits from the Accent 5 theme color</span></span>  <br/> |
|<span data-ttu-id="fdde3-121">7</span><span class="sxs-lookup"><span data-stu-id="fdde3-121">7</span></span>  <br/> |<span data-ttu-id="fdde3-122">図形の線の色は、[アクセント 6] テーマの色から継承します</span><span class="sxs-lookup"><span data-stu-id="fdde3-122">The shape line color inherits from the Accent 6 theme color</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdde3-123">解説</span><span class="sxs-lookup"><span data-stu-id="fdde3-123">Remarks</span></span>

<span data-ttu-id="fdde3-124">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleLineColor**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fdde3-124">To get a reference to the **QuickStyleLineColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdde3-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="fdde3-125">Cell name:</span></span>  <br/> | <span data-ttu-id="fdde3-126">[quickstylelinecolor]</span><span class="sxs-lookup"><span data-stu-id="fdde3-126">QuickStyleLineColor</span></span>  <br/> |
   
<span data-ttu-id="fdde3-127">プログラムから、インデックスによって [**QuickStyleLineColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fdde3-127">To get a reference to the **QuickStyleLineColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdde3-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fdde3-128">Section index:</span></span>  <br/> |<span data-ttu-id="fdde3-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fdde3-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fdde3-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fdde3-130">Row index:</span></span>  <br/> |<span data-ttu-id="fdde3-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="fdde3-131">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="fdde3-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fdde3-132">Cell index:</span></span>  <br/> |<span data-ttu-id="fdde3-133">**visQuickStyleLineColor**</span><span class="sxs-lookup"><span data-stu-id="fdde3-133">**visQuickStyleLineColor**</span></span> <br/> |
   

