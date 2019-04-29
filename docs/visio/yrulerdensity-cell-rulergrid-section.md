---
title: '[yrulerdensity] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: ページのルーラーに対して、垂直方向の小区分を指定します。
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406802"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="efbb9-103">[yrulerdensity] セル&amp; ([ルーラーグリッド] セクション)</span><span class="sxs-lookup"><span data-stu-id="efbb9-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="efbb9-104">ページのルーラーに対して、垂直方向の小区分を指定します。</span><span class="sxs-lookup"><span data-stu-id="efbb9-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="efbb9-105">**値**</span><span class="sxs-lookup"><span data-stu-id="efbb9-105">**Value**</span></span>|<span data-ttu-id="efbb9-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="efbb9-106">**Description**</span></span>|<span data-ttu-id="efbb9-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="efbb9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="efbb9-108">.0</span><span class="sxs-lookup"><span data-stu-id="efbb9-108">0</span></span>  <br/> |<span data-ttu-id="efbb9-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="efbb9-109">Fixed</span></span>  <br/> |<span data-ttu-id="efbb9-110">**visrulerfixed**</span><span class="sxs-lookup"><span data-stu-id="efbb9-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="efbb9-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="efbb9-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="efbb9-112">粗い</span><span class="sxs-lookup"><span data-stu-id="efbb9-112">Coarse</span></span>  <br/> |<span data-ttu-id="efbb9-113">**visrulercoarse**</span><span class="sxs-lookup"><span data-stu-id="efbb9-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="efbb9-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="efbb9-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="efbb9-115">標準 (既定値)</span><span class="sxs-lookup"><span data-stu-id="efbb9-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="efbb9-116">**visrulernormal**</span><span class="sxs-lookup"><span data-stu-id="efbb9-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="efbb9-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="efbb9-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="efbb9-118">いい</span><span class="sxs-lookup"><span data-stu-id="efbb9-118">Fine</span></span>  <br/> |<span data-ttu-id="efbb9-119">**visrulerfine**</span><span class="sxs-lookup"><span data-stu-id="efbb9-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efbb9-120">注釈</span><span class="sxs-lookup"><span data-stu-id="efbb9-120">Remarks</span></span>

<span data-ttu-id="efbb9-121">このセルは、[**ルーラー &amp;グリッド**] ダイアログボックス ([**表示**] タブの [**表示**] 矢印をクリック) の [垂直方向の**目盛り**] オプションに対応しています。</span><span class="sxs-lookup"><span data-stu-id="efbb9-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="efbb9-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YRulerDensity] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="efbb9-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="efbb9-123">セル名 :</span><span class="sxs-lookup"><span data-stu-id="efbb9-123">Cell name:</span></span>  <br/> |<span data-ttu-id="efbb9-124">[yrulerdensity]</span><span class="sxs-lookup"><span data-stu-id="efbb9-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="efbb9-125">プログラムから、インデックスによって [YRulerDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="efbb9-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="efbb9-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="efbb9-126">Section index:</span></span>  <br/> |<span data-ttu-id="efbb9-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="efbb9-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="efbb9-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="efbb9-128">Row index:</span></span>  <br/> |<span data-ttu-id="efbb9-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="efbb9-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="efbb9-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="efbb9-130">Cell index:</span></span>  <br/> |<span data-ttu-id="efbb9-131">**visyrulerdensity**</span><span class="sxs-lookup"><span data-stu-id="efbb9-131">**visYRulerDensity**</span></span> <br/> |
   

