---
title: '[xrulerdensity] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: ページのルーラーに対して、水平方向の小区分を指定します。
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411471"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="34562-103">[xrulerdensity] セル&amp; ([ルーラーグリッド] セクション)</span><span class="sxs-lookup"><span data-stu-id="34562-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="34562-104">ページのルーラーに対して、水平方向の小区分を指定します。</span><span class="sxs-lookup"><span data-stu-id="34562-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="34562-105">**値**</span><span class="sxs-lookup"><span data-stu-id="34562-105">**Value**</span></span>|<span data-ttu-id="34562-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="34562-106">**Description**</span></span>|<span data-ttu-id="34562-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="34562-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="34562-108">.0</span><span class="sxs-lookup"><span data-stu-id="34562-108">0</span></span>  <br/> |<span data-ttu-id="34562-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="34562-109">Fixed</span></span>  <br/> |<span data-ttu-id="34562-110">**visrulerfixed**</span><span class="sxs-lookup"><span data-stu-id="34562-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="34562-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="34562-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="34562-112">粗い</span><span class="sxs-lookup"><span data-stu-id="34562-112">Coarse</span></span>  <br/> |<span data-ttu-id="34562-113">**visrulercoarse**</span><span class="sxs-lookup"><span data-stu-id="34562-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="34562-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="34562-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="34562-115">標準 (既定値)</span><span class="sxs-lookup"><span data-stu-id="34562-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="34562-116">**visrulernormal**</span><span class="sxs-lookup"><span data-stu-id="34562-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="34562-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="34562-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="34562-118">いい</span><span class="sxs-lookup"><span data-stu-id="34562-118">Fine</span></span>  <br/> |<span data-ttu-id="34562-119">**visrulerfine**</span><span class="sxs-lookup"><span data-stu-id="34562-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34562-120">注釈</span><span class="sxs-lookup"><span data-stu-id="34562-120">Remarks</span></span>

<span data-ttu-id="34562-121">このセルは、[**ルーラー &amp;グリッド**] ダイアログボックス ([**表示**] タブの [**表示**] 矢印をクリック) の [水平方向の**目盛り**] オプションに対応しています。</span><span class="sxs-lookup"><span data-stu-id="34562-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="34562-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XRulerDensity] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="34562-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34562-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="34562-123">Cell name:</span></span>  <br/> |<span data-ttu-id="34562-124">[xrulerdensity]</span><span class="sxs-lookup"><span data-stu-id="34562-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="34562-125">プログラムから、インデックスによって [XRulerDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="34562-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34562-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="34562-126">Section index:</span></span>  <br/> |<span data-ttu-id="34562-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="34562-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="34562-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="34562-128">Row index:</span></span>  <br/> |<span data-ttu-id="34562-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="34562-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="34562-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="34562-130">Cell index:</span></span>  <br/> |<span data-ttu-id="34562-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="34562-131">**visXRulerDensity**</span></span> <br/> |
   

