---
title: '[PageShapeSplit] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: ページの図形が自動的に分割されるかどうかを示します。
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422020"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="a539f-103">[PageShapeSplit] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="a539f-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="a539f-104">ページの図形が自動的に分割されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a539f-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="a539f-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a539f-105">**Value**</span></span>|<span data-ttu-id="a539f-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a539f-106">**Description**</span></span>|<span data-ttu-id="a539f-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="a539f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a539f-108">0</span><span class="sxs-lookup"><span data-stu-id="a539f-108">0</span></span>  <br/> |<span data-ttu-id="a539f-109">図形の自動分割は許可しない。</span><span class="sxs-lookup"><span data-stu-id="a539f-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="a539f-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="a539f-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="a539f-111">1</span><span class="sxs-lookup"><span data-stu-id="a539f-111">1</span></span>  <br/> |<span data-ttu-id="a539f-112">自動図形分割を許可する (既定)。</span><span class="sxs-lookup"><span data-stu-id="a539f-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="a539f-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="a539f-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a539f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a539f-114">Remarks</span></span>

<span data-ttu-id="a539f-115">図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="a539f-115">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="a539f-116">既定では、分割はアプリケーションレベルとページ レベルで有効になっています。</span><span class="sxs-lookup"><span data-stu-id="a539f-116">By default, splitting is enabled at the application and page levels.</span></span> <span data-ttu-id="a539f-117">図形の既定の設定は、図面の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="a539f-117">The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="a539f-118">アプリケーション レベルで分割を有効または無効にするには、[Visioオプション] ダイアログボックスの [詳細設定] タブの [コネクタ分割を有効にする] 設定を使用します **(Office** ボタンをクリックし、[Visio]タブの [オプション] をクリックし、[詳細設定] をクリックします)。 </span><span class="sxs-lookup"><span data-stu-id="a539f-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="a539f-119">図形レベルでの分割を有効または無効にするには、ShapeSplit セルと ShapeSplittable セルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a539f-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="a539f-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageShapeSplit] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a539f-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a539f-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="a539f-121">Cell name:</span></span>  <br/> |<span data-ttu-id="a539f-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="a539f-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="a539f-123">プログラムからインデックスによって PageShapeSplit セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a539f-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a539f-124">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a539f-124">Section index:</span></span>  <br/> |<span data-ttu-id="a539f-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a539f-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a539f-126">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a539f-126">Row index:</span></span>  <br/> |<span data-ttu-id="a539f-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a539f-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a539f-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a539f-128">Cell index:</span></span>  <br/> |<span data-ttu-id="a539f-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="a539f-129">**visPLOSplit**</span></span> <br/> |
   

