---
title: '[QuickStyleShadowColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0a80959f-941f-451c-9049-dc661ff4930f
description: 図形の影に使用するテーマの色を、0から7の整数で指定します。
ms.openlocfilehash: b623eee89d214bade2706b12fcb344eccd8814b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414957"
---
# <a name="quickstyleshadowcolor-cell-quick-style-section"></a><span data-ttu-id="99c00-103">[QuickStyleShadowColor] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="99c00-103">QuickStyleShadowColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="99c00-104">図形の影に使用するテーマの色を、0から7の整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="99c00-104">Determines which theme color that a shape's shadow uses, as an integer from 0 to 7.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99c00-105">値</span><span class="sxs-lookup"><span data-stu-id="99c00-105">Value</span></span>  <br/> |<span data-ttu-id="99c00-106">説明</span><span class="sxs-lookup"><span data-stu-id="99c00-106">Description</span></span>  <br/> |
|<span data-ttu-id="99c00-107">.0</span><span class="sxs-lookup"><span data-stu-id="99c00-107">0</span></span>  <br/> |<span data-ttu-id="99c00-108">図形の影の色を、[ダーク] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="99c00-108">The shape shadow color inherits from the Dark theme color.</span></span>  <br/> |
|<span data-ttu-id="99c00-109">1 </span><span class="sxs-lookup"><span data-stu-id="99c00-109">1</span></span>  <br/> |<span data-ttu-id="99c00-110">図形の影の色を、[ライト] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="99c00-110">The shape shadow color inherits from the Light theme color.</span></span>  <br/> |
|<span data-ttu-id="99c00-111">2 </span><span class="sxs-lookup"><span data-stu-id="99c00-111">2</span></span>  <br/> |<span data-ttu-id="99c00-112">図形の影の色を、[アクセント 1] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="99c00-112">The shape shadow color inherits from the Accent 1 theme color.</span></span>  <br/> |
|<span data-ttu-id="99c00-113">3 </span><span class="sxs-lookup"><span data-stu-id="99c00-113">3</span></span>  <br/> |<span data-ttu-id="99c00-114">図形の影の色を、[アクセント 2] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="99c00-114">The shape shadow color inherits from the Accent 2 theme color.</span></span>  <br/> |
|<span data-ttu-id="99c00-115">4 </span><span class="sxs-lookup"><span data-stu-id="99c00-115">4</span></span>  <br/> |<span data-ttu-id="99c00-116">図形の影の色を、[アクセント 3] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="99c00-116">The shape shadow color inherits from the Accent 3 theme color.</span></span>  <br/> |
|<span data-ttu-id="99c00-117">5 </span><span class="sxs-lookup"><span data-stu-id="99c00-117">5</span></span>  <br/> |<span data-ttu-id="99c00-118">図形の影の色を、[アクセント 4] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="99c00-118">The shape shadow color inherits from the Accent 4 theme color.</span></span>  <br/> |
|<span data-ttu-id="99c00-119">6 </span><span class="sxs-lookup"><span data-stu-id="99c00-119">6</span></span>  <br/> |<span data-ttu-id="99c00-120">図形の影の色を、[アクセント 5] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="99c00-120">The shape shadow color inherits from the Accent 5 theme color.</span></span>  <br/> |
|<span data-ttu-id="99c00-121">7 </span><span class="sxs-lookup"><span data-stu-id="99c00-121">7</span></span>  <br/> |<span data-ttu-id="99c00-122">図形の影の色を、[アクセント 6] テーマの色から継承します。</span><span class="sxs-lookup"><span data-stu-id="99c00-122">The shape shadow color inherits from the Accent 6 theme color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99c00-123">注釈</span><span class="sxs-lookup"><span data-stu-id="99c00-123">Remarks</span></span>

<span data-ttu-id="99c00-124">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleShadowColor**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="99c00-124">To get a reference to the **QuickStyleShadowColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99c00-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="99c00-125">Cell name:</span></span>  <br/> | <span data-ttu-id="99c00-126">[quickstyleshadowcolor]</span><span class="sxs-lookup"><span data-stu-id="99c00-126">QuickStyleShadowColor</span></span>  <br/> |
   
<span data-ttu-id="99c00-127">プログラムから、インデックスによって[**QuickStyleShadowColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="99c00-127">To get a reference to the **QuickStyleShadowColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99c00-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="99c00-128">Section index:</span></span>  <br/> |<span data-ttu-id="99c00-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="99c00-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="99c00-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="99c00-130">Row index:</span></span>  <br/> |<span data-ttu-id="99c00-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="99c00-131">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="99c00-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="99c00-132">Cell index:</span></span>  <br/> |<span data-ttu-id="99c00-133">**visQuickStyleShadowColor**</span><span class="sxs-lookup"><span data-stu-id="99c00-133">**visQuickStyleShadowColor**</span></span> <br/> |
   

