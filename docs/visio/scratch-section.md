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
# <a name="scratch-section"></a><span data-ttu-id="092f2-103">[Scratch] セクション</span><span class="sxs-lookup"><span data-stu-id="092f2-103">Scratch Section</span></span>

<span data-ttu-id="092f2-104">他のセルが参照する数式の入力およびテストを実行するための作業領域です。</span><span class="sxs-lookup"><span data-stu-id="092f2-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="092f2-105">注釈</span><span class="sxs-lookup"><span data-stu-id="092f2-105">Remarks</span></span>

<span data-ttu-id="092f2-p101">このセクションは、[**セクションの挿入**] ダイアログ ボックスを使用して追加できます。この操作を行うには、[シェイプシート] ウィンドウで右クリックして、[**セクションの挿入**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="092f2-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="092f2-p102">通常 [**スクラッチ**] セクションは、繰り返される複雑な計算を分離するために使用します。ソリューションの目的がはっきりしている場合は、[**ユーザー定義セル**] セクションのセルを使用する方が賢明です。これは、ユーザー セルに名前を付けて明確化できるためです。</span><span class="sxs-lookup"><span data-stu-id="092f2-p102">The **Scratch** section is typically used to isolate repeated complex calculations. If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="092f2-110">[スクラッチ] セクション **のセルは** 、2 つの異なる方法で単位を使用します。</span><span class="sxs-lookup"><span data-stu-id="092f2-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="092f2-111">X セルと Y セルは図面単位を使用します。A から D のセルは単位を使用しない。</span><span class="sxs-lookup"><span data-stu-id="092f2-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="092f2-112">(C プログラマの専門用語では、X セルと Y セルは "型指定" され、セル A ~ D は "void"です)。**Scratch X** セルと Scratch **Y** セルは、多くの場合 **、PinX** や **PinY** などの *x* 座標と *y* 座標、または **[Geometry]** セクション セルにある X セルと Y セルを導き出す場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="092f2-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="092f2-113">スクラッチ セル A から D まで、指定した単位を表示できます。</span><span class="sxs-lookup"><span data-stu-id="092f2-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="092f2-114">さらに大きな違いは、これらのセルがポイント値を格納する方法にあります。</span><span class="sxs-lookup"><span data-stu-id="092f2-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="092f2-115">オブジェクト内のVisioは、 ( *x,y*) 座標の 1 つのデータ パッケージです。</span><span class="sxs-lookup"><span data-stu-id="092f2-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="092f2-116">数式がポイント値を返すと、返された値は、その数式が含まれているシェイプシート セルに応じて、次の 3 つのうちいずれかの方法で解釈されます。</span><span class="sxs-lookup"><span data-stu-id="092f2-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="092f2-117">*x* 座標に関連するセル (**たとえば、PinX、\*\*\*\*または Geometry** セクションの X 列のセル) は、ポイント値の *x* 座標部分を抽出します。</span><span class="sxs-lookup"><span data-stu-id="092f2-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="092f2-118">y 座標に  *関連するセル*  は、ポイント値  *の y*  座標部分を抽出します。</span><span class="sxs-lookup"><span data-stu-id="092f2-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="092f2-119">たとえば、次Visio 3 つの `PNT(3,4)` 方法で数式を抽出します。</span><span class="sxs-lookup"><span data-stu-id="092f2-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="092f2-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="092f2-120">**Cell**</span></span>|<span data-ttu-id="092f2-121">**入力**</span><span class="sxs-lookup"><span data-stu-id="092f2-121">**If you enter**</span></span>|<span data-ttu-id="092f2-122">**Visioとして扱う**</span><span class="sxs-lookup"><span data-stu-id="092f2-122">**Visio treats it as**</span></span>|<span data-ttu-id="092f2-123">**結果**</span><span class="sxs-lookup"><span data-stu-id="092f2-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="092f2-124">X</span><span class="sxs-lookup"><span data-stu-id="092f2-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="092f2-125">3.0000 in.</span><span class="sxs-lookup"><span data-stu-id="092f2-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="092f2-126">Y</span><span class="sxs-lookup"><span data-stu-id="092f2-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="092f2-127">4.0000 in.</span><span class="sxs-lookup"><span data-stu-id="092f2-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="092f2-128">A-D</span><span class="sxs-lookup"><span data-stu-id="092f2-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="092f2-129">PNT(3.0000 in., 4.0000 in.</span><span class="sxs-lookup"><span data-stu-id="092f2-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

