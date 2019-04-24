---
title: '[xgriddensity] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: 使用する水平方向のグリッドの種類を指定します。
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328988"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="8a249-103">[xgriddensity] セル&amp; ([ルーラーグリッド] セクション)</span><span class="sxs-lookup"><span data-stu-id="8a249-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="8a249-104">使用する水平方向のグリッドの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a249-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="8a249-105">**値**</span><span class="sxs-lookup"><span data-stu-id="8a249-105">**Value**</span></span>|<span data-ttu-id="8a249-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="8a249-106">**Description**</span></span>|<span data-ttu-id="8a249-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="8a249-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a249-108">.0</span><span class="sxs-lookup"><span data-stu-id="8a249-108">0</span></span>  <br/> |<span data-ttu-id="8a249-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="8a249-109">Fixed</span></span>  <br/> |<span data-ttu-id="8a249-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="8a249-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="8a249-111">pbm-2</span><span class="sxs-lookup"><span data-stu-id="8a249-111">2</span></span>  <br/> |<span data-ttu-id="8a249-112">粗い</span><span class="sxs-lookup"><span data-stu-id="8a249-112">Coarse</span></span>  <br/> |<span data-ttu-id="8a249-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="8a249-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="8a249-114">2/4</span><span class="sxs-lookup"><span data-stu-id="8a249-114">4</span></span>  <br/> |<span data-ttu-id="8a249-115">標準 (既定値)</span><span class="sxs-lookup"><span data-stu-id="8a249-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="8a249-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="8a249-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="8a249-117">~</span><span class="sxs-lookup"><span data-stu-id="8a249-117">8</span></span>  <br/> |<span data-ttu-id="8a249-118">いい</span><span class="sxs-lookup"><span data-stu-id="8a249-118">Fine</span></span>  <br/> |<span data-ttu-id="8a249-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="8a249-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a249-120">解説</span><span class="sxs-lookup"><span data-stu-id="8a249-120">Remarks</span></span>

<span data-ttu-id="8a249-121">このセルは、[**ルーラー &amp;グリッド**] ダイアログボックスの [上下の**間隔**] オプションに対応しています ([**表示**] タブで [**表示**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="8a249-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="8a249-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XGridDensity] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8a249-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a249-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="8a249-123">Cell name:</span></span>  <br/> |<span data-ttu-id="8a249-124">xgriddensity]</span><span class="sxs-lookup"><span data-stu-id="8a249-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="8a249-125">プログラムから、インデックスによって [XGridDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a249-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a249-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8a249-126">Section index:</span></span>  <br/> |<span data-ttu-id="8a249-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8a249-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8a249-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8a249-128">Row index:</span></span>  <br/> |<span data-ttu-id="8a249-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="8a249-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="8a249-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8a249-130">Cell index:</span></span>  <br/> |<span data-ttu-id="8a249-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="8a249-131">**visXGridDensity**</span></span> <br/> |
   

