---
title: '[QuickStyleFillColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: 図形の塗りつぶしに使用するテーマの色を、0から7の整数で指定します。
ms.openlocfilehash: 3ace0de7e3bfc878a2101eaca3847ef079b8f919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407964"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a><span data-ttu-id="c856a-103">[QuickStyleFillColor] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="c856a-103">QuickStyleFillColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="c856a-104">図形の塗りつぶしに使用するテーマの色を、0から7の整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="c856a-104">Determines which theme color that a shape's fill uses, as an integer from 0 to 7</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c856a-105">値</span><span class="sxs-lookup"><span data-stu-id="c856a-105">Value</span></span>  <br/> |<span data-ttu-id="c856a-106">説明</span><span class="sxs-lookup"><span data-stu-id="c856a-106">Description</span></span>  <br/> |
|<span data-ttu-id="c856a-107">.0</span><span class="sxs-lookup"><span data-stu-id="c856a-107">0</span></span>  <br/> |<span data-ttu-id="c856a-108">図形の塗りつぶしの色は、[ダーク] テーマの色を継承します。</span><span class="sxs-lookup"><span data-stu-id="c856a-108">The shape fill color inherits from the Dark theme color.</span></span>  <br/> |
|<span data-ttu-id="c856a-109">1 </span><span class="sxs-lookup"><span data-stu-id="c856a-109">1</span></span>  <br/> |<span data-ttu-id="c856a-110">図形の塗りつぶしの色は、[ライト] テーマの色を継承します。</span><span class="sxs-lookup"><span data-stu-id="c856a-110">The shape fill color inherits from the Light theme color.</span></span>  <br/> |
|<span data-ttu-id="c856a-111">2 </span><span class="sxs-lookup"><span data-stu-id="c856a-111">2</span></span>  <br/> |<span data-ttu-id="c856a-112">図形の塗りつぶしの色は、[アクセント 1] テーマの色を継承します</span><span class="sxs-lookup"><span data-stu-id="c856a-112">The shape fill color inherits from the Accent 1 theme color</span></span>  <br/> |
|<span data-ttu-id="c856a-113">3 </span><span class="sxs-lookup"><span data-stu-id="c856a-113">3</span></span>  <br/> |<span data-ttu-id="c856a-114">図形の塗りつぶしの色は、[アクセント 2] テーマの色を継承します</span><span class="sxs-lookup"><span data-stu-id="c856a-114">The shape fill color inherits from the Accent 2 theme color</span></span>  <br/> |
|<span data-ttu-id="c856a-115">4 </span><span class="sxs-lookup"><span data-stu-id="c856a-115">4</span></span>  <br/> |<span data-ttu-id="c856a-116">図形の塗りつぶしの色は、[アクセント 3] テーマの色を継承します</span><span class="sxs-lookup"><span data-stu-id="c856a-116">The shape fill color inherits from the Accent 3 theme color</span></span>  <br/> |
|<span data-ttu-id="c856a-117">5 </span><span class="sxs-lookup"><span data-stu-id="c856a-117">5</span></span>  <br/> |<span data-ttu-id="c856a-118">図形の塗りつぶしの色は、[アクセント 4] テーマの色を継承します</span><span class="sxs-lookup"><span data-stu-id="c856a-118">The shape fill color inherits from the Accent 4 theme color</span></span>  <br/> |
|<span data-ttu-id="c856a-119">6 </span><span class="sxs-lookup"><span data-stu-id="c856a-119">6</span></span>  <br/> |<span data-ttu-id="c856a-120">図形の塗りつぶしの色は、[アクセント 5] テーマの色を継承します</span><span class="sxs-lookup"><span data-stu-id="c856a-120">The shape fill color inherits from the Accent 5 theme color</span></span>  <br/> |
|<span data-ttu-id="c856a-121">7 </span><span class="sxs-lookup"><span data-stu-id="c856a-121">7</span></span>  <br/> |<span data-ttu-id="c856a-122">図形の塗りつぶしの色は、[アクセント 6] テーマの色を継承します</span><span class="sxs-lookup"><span data-stu-id="c856a-122">The shape fill color inherits from the Accent 6 theme color</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c856a-123">注釈</span><span class="sxs-lookup"><span data-stu-id="c856a-123">Remarks</span></span>

<span data-ttu-id="c856a-124">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleFillColor**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c856a-124">To get a reference to the **QuickStyleFillColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c856a-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="c856a-125">Cell name:</span></span>  <br/> | <span data-ttu-id="c856a-126">[quickstylefillcolor]</span><span class="sxs-lookup"><span data-stu-id="c856a-126">QuickStyleFillColor</span></span>  <br/> |
   
<span data-ttu-id="c856a-127">プログラムから、インデックスによって [**QuickStyleFillColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c856a-127">To get a reference to the **QuickStyleFillColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c856a-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c856a-128">Section index:</span></span>  <br/> |<span data-ttu-id="c856a-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c856a-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c856a-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c856a-130">Row index:</span></span>  <br/> |<span data-ttu-id="c856a-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="c856a-131">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="c856a-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c856a-132">Cell index:</span></span>  <br/> |<span data-ttu-id="c856a-133">**visQuickStyleFillColor**</span><span class="sxs-lookup"><span data-stu-id="c856a-133">**visQuickStyleFillColor**</span></span> <br/> |
   

