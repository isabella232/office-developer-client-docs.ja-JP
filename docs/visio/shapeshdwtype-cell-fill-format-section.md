---
title: '[ShapeShdwType] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: 図形の影の種類を指定します。
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342862"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="d4907-103">[ShapeShdwType] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="d4907-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="d4907-104">図形の影の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4907-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="d4907-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d4907-105">**Value**</span></span>|<span data-ttu-id="d4907-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d4907-106">**Description**</span></span>|<span data-ttu-id="d4907-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="d4907-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4907-108">.0</span><span class="sxs-lookup"><span data-stu-id="d4907-108">0</span></span>  <br/> |<span data-ttu-id="d4907-109">ページの既定値を使用します (既定値)。</span><span class="sxs-lookup"><span data-stu-id="d4907-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="d4907-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="d4907-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="d4907-111">1-d</span><span class="sxs-lookup"><span data-stu-id="d4907-111">1</span></span>  <br/> |<span data-ttu-id="d4907-112">単純</span><span class="sxs-lookup"><span data-stu-id="d4907-112">Simple</span></span>  <br/> |<span data-ttu-id="d4907-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="d4907-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="d4907-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="d4907-114">2</span></span>  <br/> |<span data-ttu-id="d4907-115">斜体</span><span class="sxs-lookup"><span data-stu-id="d4907-115">Oblique</span></span>  <br/> |<span data-ttu-id="d4907-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="d4907-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4907-117">解説</span><span class="sxs-lookup"><span data-stu-id="d4907-117">Remarks</span></span>

<span data-ttu-id="d4907-118">このセルを使用して、既定のページとは異なる図形の影を適用します (ページの既定の影の種類は、[ページのプロパティ] セクションの [[shdwtype]] セルで定義されています)。</span><span class="sxs-lookup"><span data-stu-id="d4907-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="d4907-119">シンプルな影は、ユーザー インターフェイス (UI) では "オフセット" と表示されます。</span><span class="sxs-lookup"><span data-stu-id="d4907-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="d4907-120">シンプルな影は、その図形の下の平面に影を落としているように見えます。</span><span class="sxs-lookup"><span data-stu-id="d4907-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="d4907-121">斜体の影は UI では "斜体" と表示され、その図形が直立している平面に影を落としているように見えます。</span><span class="sxs-lookup"><span data-stu-id="d4907-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="d4907-122">事前定義されたシンプルな影と斜体の影の種類のリストは、[**影**] ダイアログ ボックスの [**スタイル**] ボックスを参照してください (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="d4907-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="d4907-123">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwType] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4907-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4907-124">セル名 :</span><span class="sxs-lookup"><span data-stu-id="d4907-124">Cell name:</span></span>  <br/> |<span data-ttu-id="d4907-125">[shapeshdwtype]</span><span class="sxs-lookup"><span data-stu-id="d4907-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="d4907-126">プログラムから、インデックスによって [ShapeShdwType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4907-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4907-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4907-127">Section index:</span></span>  <br/> |<span data-ttu-id="d4907-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d4907-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d4907-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4907-129">Row index:</span></span>  <br/> |<span data-ttu-id="d4907-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="d4907-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="d4907-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4907-131">Cell index:</span></span>  <br/> |<span data-ttu-id="d4907-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="d4907-132">**visFillShdwType**</span></span> <br/> |
   

