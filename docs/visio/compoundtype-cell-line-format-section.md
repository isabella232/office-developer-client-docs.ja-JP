---
title: '[CompoundType] セル ([線の形式] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: 複合図形の線の種類を決定します。
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805054"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="45bb4-103">[CompoundType] セル ([線の形式] セクション)</span><span class="sxs-lookup"><span data-stu-id="45bb4-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="45bb4-104">複合図形の線の種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="45bb4-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="45bb4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="45bb4-105">**Value**</span></span>|<span data-ttu-id="45bb4-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="45bb4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="45bb4-107">0</span><span class="sxs-lookup"><span data-stu-id="45bb4-107">0</span></span>  <br/> |<span data-ttu-id="45bb4-108">Simple/標準</span><span class="sxs-lookup"><span data-stu-id="45bb4-108">Simple</span></span>  <br/> |
|<span data-ttu-id="45bb4-109">1</span><span class="sxs-lookup"><span data-stu-id="45bb4-109">1</span></span>  <br/> |<span data-ttu-id="45bb4-110">倍精度浮動小数点型 (Double)</span><span class="sxs-lookup"><span data-stu-id="45bb4-110">Double</span></span>  <br/> |
|<span data-ttu-id="45bb4-111">2</span><span class="sxs-lookup"><span data-stu-id="45bb4-111">2</span></span>  <br/> |<span data-ttu-id="45bb4-112">太さシンします。</span><span class="sxs-lookup"><span data-stu-id="45bb4-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="45bb4-113">3</span><span class="sxs-lookup"><span data-stu-id="45bb4-113">3</span></span>  <br/> |<span data-ttu-id="45bb4-114">細い太い</span><span class="sxs-lookup"><span data-stu-id="45bb4-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="45bb4-115">4</span><span class="sxs-lookup"><span data-stu-id="45bb4-115">4</span></span>  <br/> |<span data-ttu-id="45bb4-116">トリプル</span><span class="sxs-lookup"><span data-stu-id="45bb4-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45bb4-117">備考</span><span class="sxs-lookup"><span data-stu-id="45bb4-117">Remarks</span></span>

<span data-ttu-id="45bb4-118">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **CompoundType** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="45bb4-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45bb4-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="45bb4-119">Cell name:</span></span>  <br/> | <span data-ttu-id="45bb4-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="45bb4-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="45bb4-121">プログラムから、インデックスによって [ **CompoundType** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="45bb4-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45bb4-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="45bb4-122">Section index:</span></span>  <br/> |<span data-ttu-id="45bb4-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="45bb4-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="45bb4-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="45bb4-124">Row index:</span></span>  <br/> |<span data-ttu-id="45bb4-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="45bb4-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="45bb4-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="45bb4-126">Cell index:</span></span>  <br/> |<span data-ttu-id="45bb4-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="45bb4-127">**visCompoundType**</span></span> <br/> |
   

