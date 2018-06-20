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
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806353"
---
# <a name="scratch-section"></a><span data-ttu-id="0e815-103">[Scratch] セクション</span><span class="sxs-lookup"><span data-stu-id="0e815-103">Scratch Section</span></span>

<span data-ttu-id="0e815-104">他のセルが参照する数式の入力およびテストを実行するための作業領域です。</span><span class="sxs-lookup"><span data-stu-id="0e815-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e815-105">注釈</span><span class="sxs-lookup"><span data-stu-id="0e815-105">Remarks</span></span>

<span data-ttu-id="0e815-106">**セクションの挿入**] ダイアログ ボックスを使用して、このセクションを追加できます。</span><span class="sxs-lookup"><span data-stu-id="0e815-106">You can add this section by using the **Insert Section** dialog box.</span></span> <span data-ttu-id="0e815-107">[シェイプ シート] ウィンドウ内を右クリックし、**セクションの挿入**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e815-107">Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="0e815-108">繰り返される複雑な計算を分離するのには、[**スクラッチ**] セクションが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e815-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="0e815-109">ソリューションに適切に定義された目的がある場合は、ユーザー セルに名前を指定できるのでわかりやすくするための **[User-Defined Cells** ] セクションでセルを使用するが賢明です。</span><span class="sxs-lookup"><span data-stu-id="0e815-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="0e815-110">[**スクラッチ**] セクションのセルは、2 つの方法で単位を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e815-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="0e815-111">X セルと Y セルを使用して、図面の寸法単位です。D のセルには、ユニットを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="0e815-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="0e815-112">(C プログラマの専門用語で X と Y のセルは、型を指定、および D からのセルは、"void")**[Pinx]** と **[piny]**、または**ジオメトリ**セクションでは X と Y のセルなど、 *x 座標* *y*座標を派生するため、**スクラッチ****スクラッチ**セルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e815-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="0e815-113">A ~ D を指定する単位数を表示できるセルをスクラッチします。</span><span class="sxs-lookup"><span data-stu-id="0e815-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="0e815-114">さらに大きな違いは、これらのセルがポイント値を格納する方法です。</span><span class="sxs-lookup"><span data-stu-id="0e815-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="0e815-115">Visio におけるポイントとは、( *x, y*) 座標に対する単一のデータ パッケージです。</span><span class="sxs-lookup"><span data-stu-id="0e815-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="0e815-116">数式がポイント値を返す数式がシェイプ シート セルに応じて、3 つの方法のいずれかでその値が解釈されます。</span><span class="sxs-lookup"><span data-stu-id="0e815-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="0e815-117">*X*に関連するセルの (たとえば、 **[pinx]**、または **[Geometry** ] セクションの X カラム内のセル) の座標が*x*だけを抽出・ ポイントの値の一部を調整します。</span><span class="sxs-lookup"><span data-stu-id="0e815-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="0e815-118">*Y*に関連するセルの座標、 *y*だけを抽出する-ポイントの値の一部を調整します。</span><span class="sxs-lookup"><span data-stu-id="0e815-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="0e815-119">Visio で数式を抽出するなど、`PNT(3,4)`では、これら 3 つの方法。</span><span class="sxs-lookup"><span data-stu-id="0e815-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="0e815-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="0e815-120">**Cell**</span></span>|<span data-ttu-id="0e815-121">**入力する場合**</span><span class="sxs-lookup"><span data-stu-id="0e815-121">**If you enter**</span></span>|<span data-ttu-id="0e815-122">**Visio として扱われます**</span><span class="sxs-lookup"><span data-stu-id="0e815-122">**Visio treats it as**</span></span>|<span data-ttu-id="0e815-123">**結果**</span><span class="sxs-lookup"><span data-stu-id="0e815-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0e815-124">X</span><span class="sxs-lookup"><span data-stu-id="0e815-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="0e815-125">3.0000 に示されます。</span><span class="sxs-lookup"><span data-stu-id="0e815-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="0e815-126">Y</span><span class="sxs-lookup"><span data-stu-id="0e815-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="0e815-127">4.0000 に示されます。</span><span class="sxs-lookup"><span data-stu-id="0e815-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="0e815-128">A ~ D</span><span class="sxs-lookup"><span data-stu-id="0e815-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="0e815-129">Pnt 関数 (3.0000 インチ、4.0000 で)。</span><span class="sxs-lookup"><span data-stu-id="0e815-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

