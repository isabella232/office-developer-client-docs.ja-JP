---
title: '[ygriddensity] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: 使用する垂直方向のグリッドの種類を指定します。
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429811"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="abb5a-103">[ygriddensity] セル&amp; ([ルーラーグリッド] セクション)</span><span class="sxs-lookup"><span data-stu-id="abb5a-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="abb5a-104">使用する垂直方向のグリッドの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="abb5a-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="abb5a-105">**値**</span><span class="sxs-lookup"><span data-stu-id="abb5a-105">**Value**</span></span>|<span data-ttu-id="abb5a-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="abb5a-106">**Description**</span></span>|<span data-ttu-id="abb5a-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="abb5a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="abb5a-108">.0</span><span class="sxs-lookup"><span data-stu-id="abb5a-108">0</span></span>  <br/> |<span data-ttu-id="abb5a-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="abb5a-109">Fixed</span></span>  <br/> |<span data-ttu-id="abb5a-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="abb5a-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="abb5a-111">2 </span><span class="sxs-lookup"><span data-stu-id="abb5a-111">2</span></span>  <br/> |<span data-ttu-id="abb5a-112">粗い</span><span class="sxs-lookup"><span data-stu-id="abb5a-112">Coarse</span></span>  <br/> |<span data-ttu-id="abb5a-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="abb5a-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="abb5a-114">4 </span><span class="sxs-lookup"><span data-stu-id="abb5a-114">4</span></span>  <br/> |<span data-ttu-id="abb5a-115">標準 (既定値)</span><span class="sxs-lookup"><span data-stu-id="abb5a-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="abb5a-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="abb5a-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="abb5a-117">8 </span><span class="sxs-lookup"><span data-stu-id="abb5a-117">8</span></span>  <br/> |<span data-ttu-id="abb5a-118">いい</span><span class="sxs-lookup"><span data-stu-id="abb5a-118">Fine</span></span>  <br/> |<span data-ttu-id="abb5a-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="abb5a-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abb5a-120">注釈</span><span class="sxs-lookup"><span data-stu-id="abb5a-120">Remarks</span></span>

<span data-ttu-id="abb5a-121">このセルは、[**ルーラー &amp;グリッド**] ダイアログボックスの [上下の**間隔**] オプションに対応しています ([**表示**] タブで [**表示**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="abb5a-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="abb5a-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridDensity] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="abb5a-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="abb5a-123">セル名 :</span><span class="sxs-lookup"><span data-stu-id="abb5a-123">Cell name:</span></span>  <br/> |<span data-ttu-id="abb5a-124">ygriddensity]</span><span class="sxs-lookup"><span data-stu-id="abb5a-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="abb5a-125">プログラムから、インデックスによって [YGridDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="abb5a-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="abb5a-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="abb5a-126">Section index:</span></span>  <br/> |<span data-ttu-id="abb5a-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="abb5a-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="abb5a-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="abb5a-128">Row index:</span></span>  <br/> |<span data-ttu-id="abb5a-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="abb5a-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="abb5a-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="abb5a-130">Cell index:</span></span>  <br/> |<span data-ttu-id="abb5a-131">**visygriddensity**</span><span class="sxs-lookup"><span data-stu-id="abb5a-131">**visYGridDensity**</span></span> <br/> |
   

