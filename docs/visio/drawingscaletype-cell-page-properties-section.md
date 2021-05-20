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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428740"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="909bb-103">[DrawingScaleType] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="909bb-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="909bb-104">[**ページ設定**] ダイアログ ボックスで選択される図面縮尺を指定します (このダイアログ ボックスを開くには、[**ホーム**] タブで [**ページ設定**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="909bb-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="909bb-105">**値**</span><span class="sxs-lookup"><span data-stu-id="909bb-105">**Value**</span></span>|<span data-ttu-id="909bb-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="909bb-106">**Description**</span></span>|<span data-ttu-id="909bb-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="909bb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="909bb-108">0</span><span class="sxs-lookup"><span data-stu-id="909bb-108">0</span></span>  <br/> | <span data-ttu-id="909bb-109">等倍</span><span class="sxs-lookup"><span data-stu-id="909bb-109">No Scale</span></span>  <br/> |<span data-ttu-id="909bb-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="909bb-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="909bb-111">1</span><span class="sxs-lookup"><span data-stu-id="909bb-111">1</span></span>  <br/> | <span data-ttu-id="909bb-112">建築系縮尺</span><span class="sxs-lookup"><span data-stu-id="909bb-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="909bb-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="909bb-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="909bb-114">2</span><span class="sxs-lookup"><span data-stu-id="909bb-114">2</span></span>  <br/> | <span data-ttu-id="909bb-115">土木系縮尺</span><span class="sxs-lookup"><span data-stu-id="909bb-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="909bb-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="909bb-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="909bb-117">3</span><span class="sxs-lookup"><span data-stu-id="909bb-117">3</span></span>  <br/> | <span data-ttu-id="909bb-118">ユーザー設定の縮尺</span><span class="sxs-lookup"><span data-stu-id="909bb-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="909bb-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="909bb-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="909bb-120">4</span><span class="sxs-lookup"><span data-stu-id="909bb-120">4</span></span>  <br/> | <span data-ttu-id="909bb-121">測定基準</span><span class="sxs-lookup"><span data-stu-id="909bb-121">Metric</span></span>  <br/> |<span data-ttu-id="909bb-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="909bb-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="909bb-123">5</span><span class="sxs-lookup"><span data-stu-id="909bb-123">5</span></span>  <br/> | <span data-ttu-id="909bb-124">機械系縮尺</span><span class="sxs-lookup"><span data-stu-id="909bb-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="909bb-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="909bb-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="909bb-126">注釈</span><span class="sxs-lookup"><span data-stu-id="909bb-126">Remarks</span></span>

<span data-ttu-id="909bb-127">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DrawingScaleType] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="909bb-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="909bb-128">セル名 :</span><span class="sxs-lookup"><span data-stu-id="909bb-128">Cell name:</span></span>  <br/> | <span data-ttu-id="909bb-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="909bb-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="909bb-130">プログラムから、インデックスによって [DrawingScaleType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="909bb-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="909bb-131">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="909bb-131">Section index:</span></span>  <br/> |<span data-ttu-id="909bb-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="909bb-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="909bb-133">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="909bb-133">Row index:</span></span>  <br/> |<span data-ttu-id="909bb-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="909bb-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="909bb-135">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="909bb-135">Cell index:</span></span>  <br/> |<span data-ttu-id="909bb-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="909bb-136">**visPageDrawScaleType**</span></span> <br/> |
   

