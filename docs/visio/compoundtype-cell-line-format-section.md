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
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="f4b0c-103">[CompoundType] セル ([線の書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="f4b0c-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="f4b0c-104">複合図形の線の種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="f4b0c-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="f4b0c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f4b0c-105">**Value**</span></span>|<span data-ttu-id="f4b0c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f4b0c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4b0c-107">0</span><span class="sxs-lookup"><span data-stu-id="f4b0c-107">0</span></span>  <br/> |<span data-ttu-id="f4b0c-108">Simple/標準</span><span class="sxs-lookup"><span data-stu-id="f4b0c-108">Simple</span></span>  <br/> |
|<span data-ttu-id="f4b0c-109">1</span><span class="sxs-lookup"><span data-stu-id="f4b0c-109">1</span></span>  <br/> |<span data-ttu-id="f4b0c-110">倍精度浮動小数点数</span><span class="sxs-lookup"><span data-stu-id="f4b0c-110">Double</span></span>  <br/> |
|<span data-ttu-id="f4b0c-111">2</span><span class="sxs-lookup"><span data-stu-id="f4b0c-111">2</span></span>  <br/> |<span data-ttu-id="f4b0c-112">太さシンします。</span><span class="sxs-lookup"><span data-stu-id="f4b0c-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="f4b0c-113">3</span><span class="sxs-lookup"><span data-stu-id="f4b0c-113">3</span></span>  <br/> |<span data-ttu-id="f4b0c-114">細い太い</span><span class="sxs-lookup"><span data-stu-id="f4b0c-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="f4b0c-115">4</span><span class="sxs-lookup"><span data-stu-id="f4b0c-115">4</span></span>  <br/> |<span data-ttu-id="f4b0c-116">Triple</span><span class="sxs-lookup"><span data-stu-id="f4b0c-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4b0c-117">注釈</span><span class="sxs-lookup"><span data-stu-id="f4b0c-117">Remarks</span></span>

<span data-ttu-id="f4b0c-118">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **CompoundType** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="f4b0c-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4b0c-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="f4b0c-119">Cell name:</span></span>  <br/> | <span data-ttu-id="f4b0c-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="f4b0c-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="f4b0c-121">プログラムから、インデックスによって [ **CompoundType** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f4b0c-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4b0c-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4b0c-122">Section index:</span></span>  <br/> |<span data-ttu-id="f4b0c-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f4b0c-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f4b0c-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4b0c-124">Row index:</span></span>  <br/> |<span data-ttu-id="f4b0c-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="f4b0c-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="f4b0c-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4b0c-126">Cell index:</span></span>  <br/> |<span data-ttu-id="f4b0c-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="f4b0c-127">**visCompoundType**</span></span> <br/> |
   

