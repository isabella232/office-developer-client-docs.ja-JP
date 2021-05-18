---
title: '[CompoundType] セル ([線の形式] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: 図形の線の複合型を決定します。
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407173"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="f2499-103">[CompoundType] セル ([線の形式] セクション)</span><span class="sxs-lookup"><span data-stu-id="f2499-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="f2499-104">図形の線の複合型を決定します。</span><span class="sxs-lookup"><span data-stu-id="f2499-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="f2499-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f2499-105">**Value**</span></span>|<span data-ttu-id="f2499-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f2499-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2499-107">0</span><span class="sxs-lookup"><span data-stu-id="f2499-107">0</span></span>  <br/> |<span data-ttu-id="f2499-108">Simple/標準</span><span class="sxs-lookup"><span data-stu-id="f2499-108">Simple</span></span>  <br/> |
|<span data-ttu-id="f2499-109">1</span><span class="sxs-lookup"><span data-stu-id="f2499-109">1</span></span>  <br/> |<span data-ttu-id="f2499-110">Double</span><span class="sxs-lookup"><span data-stu-id="f2499-110">Double</span></span>  <br/> |
|<span data-ttu-id="f2499-111">2</span><span class="sxs-lookup"><span data-stu-id="f2499-111">2</span></span>  <br/> |<span data-ttu-id="f2499-112">太い薄い</span><span class="sxs-lookup"><span data-stu-id="f2499-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="f2499-113">3</span><span class="sxs-lookup"><span data-stu-id="f2499-113">3</span></span>  <br/> |<span data-ttu-id="f2499-114">薄い太さ</span><span class="sxs-lookup"><span data-stu-id="f2499-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="f2499-115">4</span><span class="sxs-lookup"><span data-stu-id="f2499-115">4</span></span>  <br/> |<span data-ttu-id="f2499-116">Triple</span><span class="sxs-lookup"><span data-stu-id="f2499-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2499-117">注釈</span><span class="sxs-lookup"><span data-stu-id="f2499-117">Remarks</span></span>

<span data-ttu-id="f2499-118">別の数式、Cell 要素 **の N** 属性の値、**または CellsU** プロパティを使用するプログラムから、名前によって **[CompoundType]** セルへの参照を取得するには、次の値を使用します。 </span><span class="sxs-lookup"><span data-stu-id="f2499-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2499-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="f2499-119">Cell name:</span></span>  <br/> | <span data-ttu-id="f2499-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="f2499-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="f2499-121">プログラムからインデックスによって **[CompoundType]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2499-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2499-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f2499-122">Section index:</span></span>  <br/> |<span data-ttu-id="f2499-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f2499-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f2499-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f2499-124">Row index:</span></span>  <br/> |<span data-ttu-id="f2499-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="f2499-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="f2499-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f2499-126">Cell index:</span></span>  <br/> |<span data-ttu-id="f2499-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="f2499-127">**visCompoundType**</span></span> <br/> |
   

