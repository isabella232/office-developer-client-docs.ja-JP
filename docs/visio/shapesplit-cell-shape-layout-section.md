---
title: '[ShapeSplit] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: この図形が、分割可能な図形を分割できるかどうかを示します。
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423560"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="5aa62-103">[ShapeSplit] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="5aa62-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="5aa62-104">この図形が、分割可能な図形を分割できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5aa62-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="5aa62-105">**値**</span><span class="sxs-lookup"><span data-stu-id="5aa62-105">**Value**</span></span>|<span data-ttu-id="5aa62-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="5aa62-106">**Description**</span></span>|<span data-ttu-id="5aa62-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="5aa62-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5aa62-108">0</span><span class="sxs-lookup"><span data-stu-id="5aa62-108">0</span></span>  <br/> | <span data-ttu-id="5aa62-109">この図形は他の図形を分割できません。</span><span class="sxs-lookup"><span data-stu-id="5aa62-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="5aa62-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="5aa62-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="5aa62-111">1</span><span class="sxs-lookup"><span data-stu-id="5aa62-111">1</span></span>  <br/> | <span data-ttu-id="5aa62-112">この図形は他の図形を分割できます。</span><span class="sxs-lookup"><span data-stu-id="5aa62-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="5aa62-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="5aa62-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5aa62-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5aa62-114">Remarks</span></span>

<span data-ttu-id="5aa62-115">他の図形を分割できる図形は、2 次元図形か 1 次元の配置可能な図形のどちらかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa62-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="5aa62-p101">図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。図形レベルでは、図面の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="5aa62-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="5aa62-118">アプリケーション レベルで分割を有効または無効にするには **、[Visio** オプション] ダイアログボックスの [詳細設定] タブの [コネクタ分割を有効にする]設定を使用します ([ファイル] タブをクリックし、[オプション] をクリックし、[詳細設定] をクリック **します)。** </span><span class="sxs-lookup"><span data-stu-id="5aa62-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="5aa62-119">ページで分割を有効または無効にするには、[PageShapeSplit] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="5aa62-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="5aa62-120">1 次元図形を分割可能にするには、[ShapeSplittable] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="5aa62-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="5aa62-121">別の数式または CellsU プロパティを使用してプログラムから名前によって [ShapeSplit] セルへの参照を取得するには、次の値 **を使用** します。</span><span class="sxs-lookup"><span data-stu-id="5aa62-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5aa62-122">セル名 :</span><span class="sxs-lookup"><span data-stu-id="5aa62-122">Cell name:</span></span>  <br/> | <span data-ttu-id="5aa62-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="5aa62-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="5aa62-124">プログラムから、インデックスによって [ShapeSplit] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5aa62-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5aa62-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5aa62-125">Section index:</span></span>  <br/> |<span data-ttu-id="5aa62-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5aa62-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5aa62-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5aa62-127">Row index:</span></span>  <br/> |<span data-ttu-id="5aa62-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="5aa62-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="5aa62-129">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5aa62-129">Cell index:</span></span>  <br/> |<span data-ttu-id="5aa62-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="5aa62-130">**visSLOSplit**</span></span> <br/> |
   

