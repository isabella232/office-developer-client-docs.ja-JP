---
title: '[ShapeSplittable] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: この 1 次元図形が分割可能かどうかを示します。
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427074"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="99ebc-103">[ShapeSplittable] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="99ebc-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="99ebc-104">この 1 次元図形が分割可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="99ebc-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="99ebc-105">**値**</span><span class="sxs-lookup"><span data-stu-id="99ebc-105">**Value**</span></span>|<span data-ttu-id="99ebc-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="99ebc-106">**Description**</span></span>|<span data-ttu-id="99ebc-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="99ebc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="99ebc-108">0</span><span class="sxs-lookup"><span data-stu-id="99ebc-108">0</span></span>  <br/> | <span data-ttu-id="99ebc-109">この図形は分割できません。</span><span class="sxs-lookup"><span data-stu-id="99ebc-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="99ebc-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="99ebc-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="99ebc-111">1</span><span class="sxs-lookup"><span data-stu-id="99ebc-111">1</span></span>  <br/> | <span data-ttu-id="99ebc-112">この図形は分割できます。</span><span class="sxs-lookup"><span data-stu-id="99ebc-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="99ebc-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="99ebc-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99ebc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="99ebc-114">Remarks</span></span>

<span data-ttu-id="99ebc-115">コネクタと他の 1 次元図形に対する既定の動作は、図面の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="99ebc-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="99ebc-p101">図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。</span><span class="sxs-lookup"><span data-stu-id="99ebc-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="99ebc-118">アプリケーション レベルで分割を有効または無効にするには **、[Visio** オプション] ダイアログボックスの [詳細設定] タブの [コネクタ分割を有効にする]設定を使用します ([ファイル] タブをクリックし、[オプション] をクリックし、[詳細設定] をクリック **します)。** </span><span class="sxs-lookup"><span data-stu-id="99ebc-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="99ebc-119">ページでの分割を有効または無効にするには、[[PageShapeSplit]](pageshapesplit-cell-page-layout-section.md) セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="99ebc-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="99ebc-120">図形が 1 次元の分割可能図形を分割できるようにするには、[[ShapeSplit]](shapesplit-cell-shape-layout-section.md) セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="99ebc-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="99ebc-121">別の数式または **CellsU** プロパティを使用してプログラムから名前によって [ShapeSplittable] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="99ebc-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99ebc-122">セル名:</span><span class="sxs-lookup"><span data-stu-id="99ebc-122">Cell name:</span></span>  <br/> | <span data-ttu-id="99ebc-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="99ebc-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="99ebc-124">プログラムから、インデックスによって [ShapeSplittable] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="99ebc-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99ebc-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="99ebc-125">Section index:</span></span>  <br/> |<span data-ttu-id="99ebc-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="99ebc-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="99ebc-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="99ebc-127">Row index:</span></span>  <br/> |<span data-ttu-id="99ebc-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="99ebc-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="99ebc-129">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="99ebc-129">Cell index:</span></span>  <br/> |<span data-ttu-id="99ebc-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="99ebc-130">**visSLOSplittable**</span></span> <br/> |
   

