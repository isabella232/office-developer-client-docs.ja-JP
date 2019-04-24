---
title: '[DrawingScaleType] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: '[ページ設定] ダイアログ ボックスで選択される図面縮尺を指定します (このダイアログ ボックスを開くには、[ホーム] タブで [ページ設定] 矢印をクリックします)。'
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359690"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="eb030-103">[DrawingScaleType] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="eb030-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="eb030-104">[**ページ設定**] ダイアログ ボックスで選択される図面縮尺を指定します (このダイアログ ボックスを開くには、[**ホーム**] タブで [**ページ設定**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="eb030-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="eb030-105">**値**</span><span class="sxs-lookup"><span data-stu-id="eb030-105">**Value**</span></span>|<span data-ttu-id="eb030-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="eb030-106">**Description**</span></span>|<span data-ttu-id="eb030-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="eb030-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="eb030-108">.0</span><span class="sxs-lookup"><span data-stu-id="eb030-108">0</span></span>  <br/> | <span data-ttu-id="eb030-109">等倍</span><span class="sxs-lookup"><span data-stu-id="eb030-109">No Scale</span></span>  <br/> |<span data-ttu-id="eb030-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="eb030-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="eb030-111">1-d</span><span class="sxs-lookup"><span data-stu-id="eb030-111">1</span></span>  <br/> | <span data-ttu-id="eb030-112">建築系縮尺</span><span class="sxs-lookup"><span data-stu-id="eb030-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="eb030-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="eb030-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="eb030-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="eb030-114">2</span></span>  <br/> | <span data-ttu-id="eb030-115">土木系縮尺</span><span class="sxs-lookup"><span data-stu-id="eb030-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="eb030-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="eb030-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="eb030-117">1/3</span><span class="sxs-lookup"><span data-stu-id="eb030-117">3</span></span>  <br/> | <span data-ttu-id="eb030-118">ユーザー設定の縮尺</span><span class="sxs-lookup"><span data-stu-id="eb030-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="eb030-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="eb030-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="eb030-120">2/4</span><span class="sxs-lookup"><span data-stu-id="eb030-120">4</span></span>  <br/> | <span data-ttu-id="eb030-121">測定基準</span><span class="sxs-lookup"><span data-stu-id="eb030-121">Metric</span></span>  <br/> |<span data-ttu-id="eb030-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="eb030-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="eb030-123">5</span><span class="sxs-lookup"><span data-stu-id="eb030-123">5</span></span>  <br/> | <span data-ttu-id="eb030-124">機械系縮尺</span><span class="sxs-lookup"><span data-stu-id="eb030-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="eb030-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="eb030-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb030-126">解説</span><span class="sxs-lookup"><span data-stu-id="eb030-126">Remarks</span></span>

<span data-ttu-id="eb030-127">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DrawingScaleType] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb030-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb030-128">セル名 :</span><span class="sxs-lookup"><span data-stu-id="eb030-128">Cell name:</span></span>  <br/> | <span data-ttu-id="eb030-129">[drawingscaletype]</span><span class="sxs-lookup"><span data-stu-id="eb030-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="eb030-130">プログラムから、インデックスによって [DrawingScaleType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eb030-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb030-131">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb030-131">Section index:</span></span>  <br/> |<span data-ttu-id="eb030-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eb030-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eb030-133">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb030-133">Row index:</span></span>  <br/> |<span data-ttu-id="eb030-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="eb030-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="eb030-135">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb030-135">Cell index:</span></span>  <br/> |<span data-ttu-id="eb030-136">**vispagedrawetype etype**</span><span class="sxs-lookup"><span data-stu-id="eb030-136">**visPageDrawScaleType**</span></span> <br/> |
   

