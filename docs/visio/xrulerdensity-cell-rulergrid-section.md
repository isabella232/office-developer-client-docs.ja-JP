---
title: '[XRulerDensity] セル ([ルーラーとグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: ページのルーラーに対して、水平方向の小区分を指定します。
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806813"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="6ad96-103">[XRulerDensity] セル ([ルーラーとグリッド] セクション)</span><span class="sxs-lookup"><span data-stu-id="6ad96-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="6ad96-104">ページのルーラーに対して、水平方向の小区分を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ad96-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="6ad96-105">**値**</span><span class="sxs-lookup"><span data-stu-id="6ad96-105">**Value**</span></span>|<span data-ttu-id="6ad96-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="6ad96-106">**Description**</span></span>|<span data-ttu-id="6ad96-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="6ad96-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6ad96-108">0</span><span class="sxs-lookup"><span data-stu-id="6ad96-108">0</span></span>  <br/> |<span data-ttu-id="6ad96-109">固定</span><span class="sxs-lookup"><span data-stu-id="6ad96-109">Fixed</span></span>  <br/> |<span data-ttu-id="6ad96-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="6ad96-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="6ad96-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="6ad96-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="6ad96-112">粗い</span><span class="sxs-lookup"><span data-stu-id="6ad96-112">Coarse</span></span>  <br/> |<span data-ttu-id="6ad96-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="6ad96-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="6ad96-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="6ad96-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="6ad96-115">標準 (既定値)</span><span class="sxs-lookup"><span data-stu-id="6ad96-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="6ad96-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="6ad96-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="6ad96-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="6ad96-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="6ad96-118">細かい</span><span class="sxs-lookup"><span data-stu-id="6ad96-118">Fine</span></span>  <br/> |<span data-ttu-id="6ad96-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="6ad96-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ad96-120">注釈</span><span class="sxs-lookup"><span data-stu-id="6ad96-120">Remarks</span></span>

<span data-ttu-id="6ad96-121">このセルの水平方向の**目盛り**オプションに対応して、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。</span><span class="sxs-lookup"><span data-stu-id="6ad96-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="6ad96-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XRulerDensity] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6ad96-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ad96-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="6ad96-123">Cell name:</span></span>  <br/> |<span data-ttu-id="6ad96-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="6ad96-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="6ad96-125">プログラムから、インデックスによって [XRulerDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ad96-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ad96-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6ad96-126">Section index:</span></span>  <br/> |<span data-ttu-id="6ad96-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6ad96-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6ad96-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6ad96-128">Row index:</span></span>  <br/> |<span data-ttu-id="6ad96-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="6ad96-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="6ad96-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6ad96-130">Cell index:</span></span>  <br/> |<span data-ttu-id="6ad96-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="6ad96-131">**visXRulerDensity**</span></span> <br/> |
   

