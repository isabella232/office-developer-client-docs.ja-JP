---
title: '[BeginArrowSiz] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: 線の開始位置にある矢印のサイズを指定します。
ms.openlocfilehash: b38e4a0685fce6d7f4aea2192ed123665eacf40a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804796"
---
# <a name="beginarrowsize-cell-line-format-section"></a><span data-ttu-id="fe633-103">[BeginArrowSize] セル ([線の書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="fe633-103">BeginArrowSize Cell (Line Format Section)</span></span>

<span data-ttu-id="fe633-104">線の開始位置にある矢印のサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="fe633-104">Determines the size of the arrowhead at the beginning of the line.</span></span>
  
|<span data-ttu-id="fe633-105">**値**</span><span class="sxs-lookup"><span data-stu-id="fe633-105">**Value**</span></span>|<span data-ttu-id="fe633-106">**Size**</span><span class="sxs-lookup"><span data-stu-id="fe633-106">**Size**</span></span>|<span data-ttu-id="fe633-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="fe633-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="fe633-108">0</span><span class="sxs-lookup"><span data-stu-id="fe633-108">0</span></span>  <br/> | <span data-ttu-id="fe633-109">極小</span><span class="sxs-lookup"><span data-stu-id="fe633-109">Very small</span></span>  <br/> |<span data-ttu-id="fe633-110">**visArrowSizeVerySmall**</span><span class="sxs-lookup"><span data-stu-id="fe633-110">**visArrowSizeVerySmall**</span></span> <br/> |
| <span data-ttu-id="fe633-111">1</span><span class="sxs-lookup"><span data-stu-id="fe633-111">1</span></span>  <br/> | <span data-ttu-id="fe633-112">小</span><span class="sxs-lookup"><span data-stu-id="fe633-112">Small</span></span>  <br/> |<span data-ttu-id="fe633-113">**visArrowSizeSmall**</span><span class="sxs-lookup"><span data-stu-id="fe633-113">**visArrowSizeSmall**</span></span> <br/> |
| <span data-ttu-id="fe633-114">2</span><span class="sxs-lookup"><span data-stu-id="fe633-114">2</span></span>  <br/> | <span data-ttu-id="fe633-115">中</span><span class="sxs-lookup"><span data-stu-id="fe633-115">Medium</span></span>  <br/> |<span data-ttu-id="fe633-116">**visArrowSizeMedium**</span><span class="sxs-lookup"><span data-stu-id="fe633-116">**visArrowSizeMedium**</span></span> <br/> |
| <span data-ttu-id="fe633-117">3</span><span class="sxs-lookup"><span data-stu-id="fe633-117">3</span></span>  <br/> | <span data-ttu-id="fe633-118">大</span><span class="sxs-lookup"><span data-stu-id="fe633-118">Large</span></span>  <br/> |<span data-ttu-id="fe633-119">**visArrowSizeLarge**</span><span class="sxs-lookup"><span data-stu-id="fe633-119">**visArrowSizeLarge**</span></span> <br/> |
| <span data-ttu-id="fe633-120">4</span><span class="sxs-lookup"><span data-stu-id="fe633-120">4</span></span>  <br/> | <span data-ttu-id="fe633-121">特大</span><span class="sxs-lookup"><span data-stu-id="fe633-121">Very large</span></span>  <br/> |<span data-ttu-id="fe633-122">**visArrowSizeVeryLarge**</span><span class="sxs-lookup"><span data-stu-id="fe633-122">**visArrowSizeVeryLarge**</span></span> <br/> |
| <span data-ttu-id="fe633-123">5</span><span class="sxs-lookup"><span data-stu-id="fe633-123">5</span></span>  <br/> | <span data-ttu-id="fe633-124">超特大</span><span class="sxs-lookup"><span data-stu-id="fe633-124">Jumbo</span></span>  <br/> |<span data-ttu-id="fe633-125">**visArrowSizeJumbo**</span><span class="sxs-lookup"><span data-stu-id="fe633-125">**visArrowSizeJumbo**</span></span> <br/> |
| <span data-ttu-id="fe633-126">6</span><span class="sxs-lookup"><span data-stu-id="fe633-126">6</span></span>  <br/> | <span data-ttu-id="fe633-127">巨大</span><span class="sxs-lookup"><span data-stu-id="fe633-127">Colossal</span></span>  <br/> |<span data-ttu-id="fe633-128">**visArrowSizeColossal**</span><span class="sxs-lookup"><span data-stu-id="fe633-128">**visArrowSizeColossal**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe633-129">注釈</span><span class="sxs-lookup"><span data-stu-id="fe633-129">Remarks</span></span>

<span data-ttu-id="fe633-130">矢印のサイズは [**線**] ダイアログ ボックスでも設定できます。</span><span class="sxs-lookup"><span data-stu-id="fe633-130">You can also set the size of the arrowhead in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="fe633-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginArrowSize] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fe633-131">To get a reference to the BeginArrowSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe633-132">セル名 :</span><span class="sxs-lookup"><span data-stu-id="fe633-132">Cell name:</span></span>  <br/> | <span data-ttu-id="fe633-133">BeginArrowSize</span><span class="sxs-lookup"><span data-stu-id="fe633-133">BeginArrowSize</span></span>  <br/> |
   
<span data-ttu-id="fe633-134">プログラムから、インデックスによって [BeginArrowSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fe633-134">To get a reference to the BeginArrowSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe633-135">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fe633-135">Section index:</span></span>  <br/> |<span data-ttu-id="fe633-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fe633-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fe633-137">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fe633-137">Row index:</span></span>  <br/> |<span data-ttu-id="fe633-138">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="fe633-138">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="fe633-139">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fe633-139">Cell index:</span></span>  <br/> |<span data-ttu-id="fe633-140">**visLineBeginArrowSize**</span><span class="sxs-lookup"><span data-stu-id="fe633-140">**visLineBeginArrowSize**</span></span> <br/> |
   

