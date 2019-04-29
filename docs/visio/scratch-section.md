---
title: '[Scratch] セクション'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: 他のセルが参照する数式の入力およびテストを実行するための作業領域です。
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411604"
---
# <a name="scratch-section"></a><span data-ttu-id="ac0ea-103">[Scratch] セクション</span><span class="sxs-lookup"><span data-stu-id="ac0ea-103">Scratch Section</span></span>

<span data-ttu-id="ac0ea-104">他のセルが参照する数式の入力およびテストを実行するための作業領域です。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ac0ea-105">注釈</span><span class="sxs-lookup"><span data-stu-id="ac0ea-105">Remarks</span></span>

<span data-ttu-id="ac0ea-p101">このセクションは、[**セクションの挿入**] ダイアログ ボックスを使用して追加できます。この操作を行うには、[シェイプシート] ウィンドウで右クリックして、[**セクションの挿入**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="ac0ea-p102">通常 [**スクラッチ**] セクションは、繰り返される複雑な計算を分離するために使用します。ソリューションの目的がはっきりしている場合は、[**ユーザー定義セル**] セクションのセルを使用する方が賢明です。これは、ユーザー セルに名前を付けて明確化できるためです。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-p102">The **Scratch** section is typically used to isolate repeated complex calculations. If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="ac0ea-110">**スクラッチ**セクションのセルは、2つの異なる方法で単位を使用します。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="ac0ea-111">X および Y セルは、描画単位を使用します。A ~ D 個のセルは単位を使用しません。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="ac0ea-112">(C プログラマの場合は、X と Y のセルは "型付けされて"、セル A から D は "void" になります)。[**スクラッチ X** ] および [**スクラッチ y** ] セルは、 **PinX** 、 **PinY**などの*x*座標と*y*座標を派生させるため、または [ **Geometry** ] セクションのセルにある [x] および [y] セルを使用する場合によく使用されます。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="ac0ea-113">スクラッチセル A から D は、指定した任意の単位を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="ac0ea-114">さらに大きな違いは、これらのセルがポイント値を格納する方法にあります。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="ac0ea-115">Visio のポイントは、( *x, y*) 座標用の1つのデータパッケージです。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="ac0ea-116">数式がポイント値を返すと、返された値は、その数式が含まれているシェイプシート セルに応じて、次の 3 つのうちいずれかの方法で解釈されます。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="ac0ea-117">*x*座標に関連するセル (たとえば、 **PinX**、または [ **Geometry** ] セクションの x 列のセル) は、ポイント値の*x*座標部分だけを抽出します。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="ac0ea-118">*y*座標に関連するセルは、ポイント値の*y*座標部分だけを抽出します。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="ac0ea-119">たとえば、Visio はこれらの 3 `PNT(3,4)`つの方法で数式を抽出します。</span><span class="sxs-lookup"><span data-stu-id="ac0ea-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="ac0ea-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ac0ea-120">**Cell**</span></span>|<span data-ttu-id="ac0ea-121">**入力**</span><span class="sxs-lookup"><span data-stu-id="ac0ea-121">**If you enter**</span></span>|<span data-ttu-id="ac0ea-122">**Visio では、**</span><span class="sxs-lookup"><span data-stu-id="ac0ea-122">**Visio treats it as**</span></span>|<span data-ttu-id="ac0ea-123">**結果**</span><span class="sxs-lookup"><span data-stu-id="ac0ea-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ac0ea-124">X</span><span class="sxs-lookup"><span data-stu-id="ac0ea-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="ac0ea-125">3.0000 in.</span><span class="sxs-lookup"><span data-stu-id="ac0ea-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="ac0ea-126">Y</span><span class="sxs-lookup"><span data-stu-id="ac0ea-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="ac0ea-127">4.0000 in.</span><span class="sxs-lookup"><span data-stu-id="ac0ea-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="ac0ea-128">A-D</span><span class="sxs-lookup"><span data-stu-id="ac0ea-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="ac0ea-129">PNT (3.0000 in.、4.0000 in)</span><span class="sxs-lookup"><span data-stu-id="ac0ea-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

