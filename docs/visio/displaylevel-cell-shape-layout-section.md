---
title: '[DisplayLevel] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: 図形の表示レベル バンド (Z オーダー グループ化の相対範囲) を指定します。
ms.openlocfilehash: 516446b2d401aaca614e24a2c5bb5003fafe8574
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805213"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="887e2-103">[DisplayLevel] セル ([図形レイアウト] セクション)</span><span class="sxs-lookup"><span data-stu-id="887e2-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="887e2-104">図形の表示レベル バンド (Z オーダー グループ化の相対範囲) を指定します。</span><span class="sxs-lookup"><span data-stu-id="887e2-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="887e2-105">注釈</span><span class="sxs-lookup"><span data-stu-id="887e2-105">Remarks</span></span>

<span data-ttu-id="887e2-p101">Z オーダーは、図面ページの図形の表示順序です。図形の 1 つが他の図形の上に重なっている場合、Z オーダーが大きい図形が Z オーダーの小さい図形の前面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="887e2-p101">Z-order is the display order for shapes on the drawing page. A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="887e2-p102">表示レベルは、図形をグループ、つまりバンドに分割します。指定されたバンド内のすべての図形に、下位バンドの図形よりも大きい Z オーダーが設定されます。既定では、ほとんどの図形の表示レベルはゼロ (0) になります。</span><span class="sxs-lookup"><span data-stu-id="887e2-p102">The display level divides shapes into groupings, or bands. All shapes in a given band have a higher Z-order than the shapes in a lower band. By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="887e2-p103">表示レベルの範囲は、-32,767 ～ +32,767 です。表示レベルが同じ図形は 1 つのバンドに結合され、そのバンド内でも Z オーダーを基準にしてランクが付けられます。</span><span class="sxs-lookup"><span data-stu-id="887e2-p103">The range of display levels is from -32,767 to +32,767. Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="887e2-113">バンド内の図形の Z オーダーを変更するには、**前面**、**背面****最前面へ移動**、および**最背面へ移動**コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="887e2-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="887e2-114">場合はこれらのコマンドは、その特定の帯域外の図形を移動、Microsoft Visio は、セルは保護されていない限り、図形のセルに DisplayLevel、-32768 の予約済みの値を表示します。</span><span class="sxs-lookup"><span data-stu-id="887e2-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="887e2-115">その場合は、別のバンドでは、図形を移動することはできませんし、警告が表示されます「図形の保護またはレイヤー プロパティは、このコマンドの完全な実行を禁止する」です。</span><span class="sxs-lookup"><span data-stu-id="887e2-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="887e2-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DisplayLevel] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="887e2-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="887e2-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="887e2-117">Cell name:</span></span>  <br/> |<span data-ttu-id="887e2-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="887e2-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="887e2-119">プログラムから、インデックスによって [DisplayLevel] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="887e2-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="887e2-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="887e2-120">Section index:</span></span>  <br/> |<span data-ttu-id="887e2-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="887e2-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="887e2-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="887e2-122">Row index:</span></span>  <br/> |<span data-ttu-id="887e2-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="887e2-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="887e2-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="887e2-124">Cell index:</span></span>  <br/> |<span data-ttu-id="887e2-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="887e2-125">**visSLODisplayLevel**</span></span> <br/> |
   

