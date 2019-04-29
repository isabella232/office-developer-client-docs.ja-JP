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
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="b5bb2-103">[PageShapeSplit] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="b5bb2-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="b5bb2-104">ページの図形が自動的に分割されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="b5bb2-105">**値**</span><span class="sxs-lookup"><span data-stu-id="b5bb2-105">**Value**</span></span>|<span data-ttu-id="b5bb2-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="b5bb2-106">**Description**</span></span>|<span data-ttu-id="b5bb2-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="b5bb2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b5bb2-108">.0</span><span class="sxs-lookup"><span data-stu-id="b5bb2-108">0</span></span>  <br/> |<span data-ttu-id="b5bb2-109">図形の自動分割を許可しません。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="b5bb2-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="b5bb2-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="b5bb2-111">1 </span><span class="sxs-lookup"><span data-stu-id="b5bb2-111">1</span></span>  <br/> |<span data-ttu-id="b5bb2-112">図形の自動分割を許可します (既定値)。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="b5bb2-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="b5bb2-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5bb2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b5bb2-114">Remarks</span></span>

<span data-ttu-id="b5bb2-115">図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-115">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="b5bb2-116">既定では、アプリケーションレベルとページレベルでスプリットが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-116">By default, splitting is enabled at the application and page levels.</span></span> <span data-ttu-id="b5bb2-117">図形の既定の設定は、図面の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-117">The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="b5bb2-118">アプリケーションレベルで分割を有効または無効にするには、[ **visio のオプション**] ダイアログボックスの [**詳細**設定] タブにある [**コネクタ分割を有効**にする] 設定を使用します ( **Office**ボタンをクリックし、 **visio**の [**オプション**] をクリックします)。tab キーを押し、[**詳細設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="b5bb2-119">図形レベルで分割を有効または無効にするには、[図形] 図形のセルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="b5bb2-120">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [[pageshapesplit]] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5bb2-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="b5bb2-121">Cell name:</span></span>  <br/> |<span data-ttu-id="b5bb2-122">[pageshapesplit]</span><span class="sxs-lookup"><span data-stu-id="b5bb2-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="b5bb2-123">プログラムから、インデックスによって [[pageshapesplit]] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5bb2-124">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b5bb2-124">Section index:</span></span>  <br/> |<span data-ttu-id="b5bb2-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b5bb2-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b5bb2-126">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b5bb2-126">Row index:</span></span>  <br/> |<span data-ttu-id="b5bb2-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b5bb2-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b5bb2-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b5bb2-128">Cell index:</span></span>  <br/> |<span data-ttu-id="b5bb2-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="b5bb2-129">**visPLOSplit**</span></span> <br/> |
   

