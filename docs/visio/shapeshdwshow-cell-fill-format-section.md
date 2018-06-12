---
title: '[ShapeShdwShow] セル ([塗りつぶしの書式設定] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: 図形に影を表示するかどうかを、0 から 2 の整数で決定します。
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806421"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="d1d36-103">[ShapeShdwShow] セル ([塗りつぶしの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="d1d36-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="d1d36-104">図形に影を表示するかどうかを、0 から 2 の整数で決定します。</span><span class="sxs-lookup"><span data-stu-id="d1d36-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="d1d36-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d1d36-105">**Value**</span></span>|<span data-ttu-id="d1d36-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d1d36-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1d36-107">0</span><span class="sxs-lookup"><span data-stu-id="d1d36-107">0</span></span>  <br/> |<span data-ttu-id="d1d36-p101">影が指定されている場合は、常に影を表示します。サブ図形の影は表示されません。</span><span class="sxs-lookup"><span data-stu-id="d1d36-p101">Always display the shadow if a shadow is specified. The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="d1d36-110">1</span><span class="sxs-lookup"><span data-stu-id="d1d36-110">1</span></span>  <br/> |<span data-ttu-id="d1d36-p102">図形の親が存在しない場合を除き、影を表示しません。共にグループ化されている場合は、サブ図形の影を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1d36-p102">Do not render a shadow unless the shape does not have a parent. Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="d1d36-113">2</span><span class="sxs-lookup"><span data-stu-id="d1d36-113">2</span></span>  <br/> |<span data-ttu-id="d1d36-p103">影が指定されている場合は、常に影を表示します。サブ図形の影も表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1d36-p103">Always display a shadow if a shadow is specified. The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1d36-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="d1d36-116">Remarks</span></span>

<span data-ttu-id="d1d36-117">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ShapeShdwShow** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d1d36-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1d36-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="d1d36-118">Cell name:</span></span>  <br/> | <span data-ttu-id="d1d36-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="d1d36-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="d1d36-120">プログラムから、インデックスによって [ **ShapeShdwShow** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d1d36-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1d36-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1d36-121">Section index:</span></span>  <br/> |<span data-ttu-id="d1d36-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d1d36-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d1d36-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1d36-123">Row index:</span></span>  <br/> |<span data-ttu-id="d1d36-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="d1d36-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="d1d36-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1d36-125">Cell index:</span></span>  <br/> |<span data-ttu-id="d1d36-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="d1d36-126">**visFillShdwShow**</span></span> <br/> |
   

