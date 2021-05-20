---
title: '[YGridDensity] セル (Ruler &amp; Grid セクション)'
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
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="50d97-103">[YGridDensity] セル (Ruler &amp; Grid セクション)</span><span class="sxs-lookup"><span data-stu-id="50d97-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="50d97-104">使用する垂直方向のグリッドの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="50d97-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="50d97-105">**値**</span><span class="sxs-lookup"><span data-stu-id="50d97-105">**Value**</span></span>|<span data-ttu-id="50d97-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="50d97-106">**Description**</span></span>|<span data-ttu-id="50d97-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="50d97-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="50d97-108">0</span><span class="sxs-lookup"><span data-stu-id="50d97-108">0</span></span>  <br/> |<span data-ttu-id="50d97-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="50d97-109">Fixed</span></span>  <br/> |<span data-ttu-id="50d97-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="50d97-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="50d97-111">2</span><span class="sxs-lookup"><span data-stu-id="50d97-111">2</span></span>  <br/> |<span data-ttu-id="50d97-112">粗い</span><span class="sxs-lookup"><span data-stu-id="50d97-112">Coarse</span></span>  <br/> |<span data-ttu-id="50d97-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="50d97-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="50d97-114">4</span><span class="sxs-lookup"><span data-stu-id="50d97-114">4</span></span>  <br/> |<span data-ttu-id="50d97-115">標準 (既定値)</span><span class="sxs-lookup"><span data-stu-id="50d97-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="50d97-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="50d97-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="50d97-117">8</span><span class="sxs-lookup"><span data-stu-id="50d97-117">8</span></span>  <br/> |<span data-ttu-id="50d97-118">いい</span><span class="sxs-lookup"><span data-stu-id="50d97-118">Fine</span></span>  <br/> |<span data-ttu-id="50d97-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="50d97-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50d97-120">注釈</span><span class="sxs-lookup"><span data-stu-id="50d97-120">Remarks</span></span>

<span data-ttu-id="50d97-121">このセルは、[ルーラーグリッド] ダイアログ ボックスの [垂直グリッド間隔] オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;**</span><span class="sxs-lookup"><span data-stu-id="50d97-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="50d97-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridDensity] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50d97-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50d97-123">セル名 :</span><span class="sxs-lookup"><span data-stu-id="50d97-123">Cell name:</span></span>  <br/> |<span data-ttu-id="50d97-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="50d97-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="50d97-125">プログラムから、インデックスによって [YGridDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="50d97-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50d97-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="50d97-126">Section index:</span></span>  <br/> |<span data-ttu-id="50d97-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="50d97-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="50d97-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="50d97-128">Row index:</span></span>  <br/> |<span data-ttu-id="50d97-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="50d97-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="50d97-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="50d97-130">Cell index:</span></span>  <br/> |<span data-ttu-id="50d97-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="50d97-131">**visYGridDensity**</span></span> <br/> |
   

