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
ms.openlocfilehash: b782977bd5b7e828223675eb16f4e7e48f4ca55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806428"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="3d4e2-103">[ShapeSplit] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="3d4e2-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="3d4e2-104">この図形が、分割可能な図形を分割できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="3d4e2-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3d4e2-105">**Value**</span></span>|<span data-ttu-id="3d4e2-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="3d4e2-106">**Description**</span></span>|<span data-ttu-id="3d4e2-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="3d4e2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3d4e2-108">0</span><span class="sxs-lookup"><span data-stu-id="3d4e2-108">0</span></span>  <br/> | <span data-ttu-id="3d4e2-109">この図形は他の図形を分割できません。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="3d4e2-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="3d4e2-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="3d4e2-111">1</span><span class="sxs-lookup"><span data-stu-id="3d4e2-111">1</span></span>  <br/> | <span data-ttu-id="3d4e2-112">この図形は他の図形を分割できます。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="3d4e2-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="3d4e2-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d4e2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3d4e2-114">Remarks</span></span>

<span data-ttu-id="3d4e2-115">他の図形を分割できる図形は、2 次元図形か 1 次元の配置可能な図形のどちらかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="3d4e2-p101">図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。図形レベルでは、図面の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="3d4e2-118">アプリケーション レベルで分割を無効にするを有効または、 **Visio のオプション**] ダイアログ ボックスの [**詳細設定**] タブに**コネクタ分割を有効にする**設定を使用して、([**ファイル**] タブをクリックして、**オプション**] をクリックし、 **高度な**)。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="3d4e2-119">ページで分割を有効または無効にするには、[PageShapeSplit] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="3d4e2-120">1 次元図形を分割可能にするには、[ShapeSplittable] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="3d4e2-121">取得する [shapesplit] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d4e2-122">セル名 :</span><span class="sxs-lookup"><span data-stu-id="3d4e2-122">Cell name:</span></span>  <br/> | <span data-ttu-id="3d4e2-123">[Shapesplit]</span><span class="sxs-lookup"><span data-stu-id="3d4e2-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="3d4e2-124">プログラムから、インデックスによって [shapesplit] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d4e2-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d4e2-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3d4e2-125">Section index:</span></span>  <br/> |<span data-ttu-id="3d4e2-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3d4e2-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3d4e2-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3d4e2-127">Row index:</span></span>  <br/> |<span data-ttu-id="3d4e2-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="3d4e2-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="3d4e2-129">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3d4e2-129">Cell index:</span></span>  <br/> |<span data-ttu-id="3d4e2-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="3d4e2-130">**visSLOSplit**</span></span> <br/> |
   

