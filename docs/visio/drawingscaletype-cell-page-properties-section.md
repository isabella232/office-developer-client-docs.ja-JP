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
description: '[ページ設定] ダイアログ ボックスで選択した図面の縮尺を指定 ([ホーム] タブの [ページ設定の矢印] をクリック) します。'
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805285"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="eb764-103">[DrawingScaleType] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="eb764-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="eb764-104">**[ページ設定**] ダイアログ ボックスで選択した図面の縮尺を指定 ([**ホーム**] タブの **[ページ設定**の矢印をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="eb764-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="eb764-105">**値**</span><span class="sxs-lookup"><span data-stu-id="eb764-105">**Value**</span></span>|<span data-ttu-id="eb764-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="eb764-106">**Description**</span></span>|<span data-ttu-id="eb764-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="eb764-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="eb764-108">0</span><span class="sxs-lookup"><span data-stu-id="eb764-108">0</span></span>  <br/> | <span data-ttu-id="eb764-109">等倍</span><span class="sxs-lookup"><span data-stu-id="eb764-109">No Scale</span></span>  <br/> |<span data-ttu-id="eb764-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="eb764-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="eb764-111">1</span><span class="sxs-lookup"><span data-stu-id="eb764-111">1</span></span>  <br/> | <span data-ttu-id="eb764-112">建築系縮尺</span><span class="sxs-lookup"><span data-stu-id="eb764-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="eb764-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="eb764-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="eb764-114">2</span><span class="sxs-lookup"><span data-stu-id="eb764-114">2</span></span>  <br/> | <span data-ttu-id="eb764-115">土木系縮尺</span><span class="sxs-lookup"><span data-stu-id="eb764-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="eb764-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="eb764-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="eb764-117">3</span><span class="sxs-lookup"><span data-stu-id="eb764-117">3</span></span>  <br/> | <span data-ttu-id="eb764-118">ユーザー設定の縮尺</span><span class="sxs-lookup"><span data-stu-id="eb764-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="eb764-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="eb764-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="eb764-120">4</span><span class="sxs-lookup"><span data-stu-id="eb764-120">4</span></span>  <br/> | <span data-ttu-id="eb764-121">メートル法</span><span class="sxs-lookup"><span data-stu-id="eb764-121">Metric</span></span>  <br/> |<span data-ttu-id="eb764-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="eb764-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="eb764-123">5</span><span class="sxs-lookup"><span data-stu-id="eb764-123">5</span></span>  <br/> | <span data-ttu-id="eb764-124">機械系縮尺</span><span class="sxs-lookup"><span data-stu-id="eb764-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="eb764-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="eb764-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb764-126">備考</span><span class="sxs-lookup"><span data-stu-id="eb764-126">Remarks</span></span>

<span data-ttu-id="eb764-127">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DrawingScaleType] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="eb764-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb764-128">セル名 :</span><span class="sxs-lookup"><span data-stu-id="eb764-128">Cell name:</span></span>  <br/> | <span data-ttu-id="eb764-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="eb764-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="eb764-130">プログラムから、インデックスによって [DrawingScaleType] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb764-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb764-131">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb764-131">Section index:</span></span>  <br/> |<span data-ttu-id="eb764-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eb764-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eb764-133">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb764-133">Row index:</span></span>  <br/> |<span data-ttu-id="eb764-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="eb764-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="eb764-135">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb764-135">Cell index:</span></span>  <br/> |<span data-ttu-id="eb764-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="eb764-136">**visPageDrawScaleType**</span></span> <br/> |
   

