---
title: '[YGridDensity] セル ([ルーラーとグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: 使用する垂直方向のグリッドの種類を指定します。
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806847"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="28b9b-103">[YGridDensity] セル ([ルーラーとグリッド] セクション)</span><span class="sxs-lookup"><span data-stu-id="28b9b-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="28b9b-104">使用する垂直方向のグリッドの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="28b9b-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="28b9b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="28b9b-105">**Value**</span></span>|<span data-ttu-id="28b9b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="28b9b-106">**Description**</span></span>|<span data-ttu-id="28b9b-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="28b9b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="28b9b-108">0</span><span class="sxs-lookup"><span data-stu-id="28b9b-108">0</span></span>  <br/> |<span data-ttu-id="28b9b-109">固定</span><span class="sxs-lookup"><span data-stu-id="28b9b-109">Fixed</span></span>  <br/> |<span data-ttu-id="28b9b-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="28b9b-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="28b9b-111">2</span><span class="sxs-lookup"><span data-stu-id="28b9b-111">2</span></span>  <br/> |<span data-ttu-id="28b9b-112">粗い</span><span class="sxs-lookup"><span data-stu-id="28b9b-112">Coarse</span></span>  <br/> |<span data-ttu-id="28b9b-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="28b9b-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="28b9b-114">4</span><span class="sxs-lookup"><span data-stu-id="28b9b-114">4</span></span>  <br/> |<span data-ttu-id="28b9b-115">標準 (既定値)</span><span class="sxs-lookup"><span data-stu-id="28b9b-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="28b9b-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="28b9b-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="28b9b-117">8</span><span class="sxs-lookup"><span data-stu-id="28b9b-117">8</span></span>  <br/> |<span data-ttu-id="28b9b-118">細かい</span><span class="sxs-lookup"><span data-stu-id="28b9b-118">Fine</span></span>  <br/> |<span data-ttu-id="28b9b-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="28b9b-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28b9b-120">注釈</span><span class="sxs-lookup"><span data-stu-id="28b9b-120">Remarks</span></span>

<span data-ttu-id="28b9b-121">このセルは、垂直方向の**グリッド線の間隔**に対応するオプションで、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。</span><span class="sxs-lookup"><span data-stu-id="28b9b-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="28b9b-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridDensity] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="28b9b-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28b9b-123">セル名 :</span><span class="sxs-lookup"><span data-stu-id="28b9b-123">Cell name:</span></span>  <br/> |<span data-ttu-id="28b9b-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="28b9b-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="28b9b-125">プログラムから、インデックスによって [YGridDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="28b9b-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28b9b-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="28b9b-126">Section index:</span></span>  <br/> |<span data-ttu-id="28b9b-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="28b9b-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="28b9b-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="28b9b-128">Row index:</span></span>  <br/> |<span data-ttu-id="28b9b-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="28b9b-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="28b9b-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="28b9b-130">Cell index:</span></span>  <br/> |<span data-ttu-id="28b9b-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="28b9b-131">**visYGridDensity**</span></span> <br/> |
   

