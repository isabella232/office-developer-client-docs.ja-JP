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
ms.openlocfilehash: e2db881465a19b34d5788f1621f15c4d7d15c293
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806435"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="41b16-103">[ShapeSplittable] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="41b16-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="41b16-104">この 1 次元図形が分割可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="41b16-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="41b16-105">**値**</span><span class="sxs-lookup"><span data-stu-id="41b16-105">**Value**</span></span>|<span data-ttu-id="41b16-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="41b16-106">**Description**</span></span>|<span data-ttu-id="41b16-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="41b16-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="41b16-108">0</span><span class="sxs-lookup"><span data-stu-id="41b16-108">0</span></span>  <br/> | <span data-ttu-id="41b16-109">この図形は分割できません。</span><span class="sxs-lookup"><span data-stu-id="41b16-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="41b16-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="41b16-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="41b16-111">1</span><span class="sxs-lookup"><span data-stu-id="41b16-111">1</span></span>  <br/> | <span data-ttu-id="41b16-112">この図形は分割できます。</span><span class="sxs-lookup"><span data-stu-id="41b16-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="41b16-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="41b16-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41b16-114">注釈</span><span class="sxs-lookup"><span data-stu-id="41b16-114">Remarks</span></span>

<span data-ttu-id="41b16-115">コネクタと他の 1 次元図形に対する既定の動作は、図面の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="41b16-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="41b16-p101">図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。</span><span class="sxs-lookup"><span data-stu-id="41b16-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="41b16-118">アプリケーション レベルで分割を無効にするを有効または、 **Visio のオプション**] ダイアログ ボックスの [**詳細設定**] タブに**コネクタ分割を有効にする**設定を使用して、([**ファイル**] タブをクリックして、**オプション**] をクリックし、 **高度な**)。</span><span class="sxs-lookup"><span data-stu-id="41b16-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="41b16-119">ページの分割を無効にするを有効または、 [PageShapeSplit](pageshapesplit-cell-page-layout-section.md)のセルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="41b16-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="41b16-120">1 次元の分割可能図形を分割できる図形には、 [[shapesplit]](shapesplit-cell-shape-layout-section.md)セルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="41b16-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="41b16-121">取得する、[ShapeSplittable] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="41b16-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41b16-122">セル名:</span><span class="sxs-lookup"><span data-stu-id="41b16-122">Cell name:</span></span>  <br/> | <span data-ttu-id="41b16-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="41b16-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="41b16-124">プログラムから、インデックスによって [ShapeSplittable] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="41b16-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41b16-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="41b16-125">Section index:</span></span>  <br/> |<span data-ttu-id="41b16-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41b16-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="41b16-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="41b16-127">Row index:</span></span>  <br/> |<span data-ttu-id="41b16-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="41b16-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="41b16-129">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="41b16-129">Cell index:</span></span>  <br/> |<span data-ttu-id="41b16-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="41b16-130">**visSLOSplittable**</span></span> <br/> |
   

