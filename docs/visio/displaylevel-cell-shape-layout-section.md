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
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408146"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="3e566-103">[DisplayLevel] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="3e566-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="3e566-104">図形の表示レベル バンド (Z オーダー グループ化の相対範囲) を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e566-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3e566-105">注釈</span><span class="sxs-lookup"><span data-stu-id="3e566-105">Remarks</span></span>

<span data-ttu-id="3e566-p101">Z オーダーは、図面ページの図形の表示順序です。図形の 1 つが他の図形の上に重なっている場合、Z オーダーが大きい図形が Z オーダーの小さい図形の前面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3e566-p101">Z-order is the display order for shapes on the drawing page. A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="3e566-p102">表示レベルは、図形をグループ、つまりバンドに分割します。指定されたバンド内のすべての図形に、下位バンドの図形よりも大きい Z オーダーが設定されます。既定では、ほとんどの図形の表示レベルはゼロ (0) になります。</span><span class="sxs-lookup"><span data-stu-id="3e566-p102">The display level divides shapes into groupings, or bands. All shapes in a given band have a higher Z-order than the shapes in a lower band. By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="3e566-p103">表示レベルの範囲は、-32,767 ～ +32,767 です。表示レベルが同じ図形は 1 つのバンドに結合され、そのバンド内でも Z オーダーを基準にしてランクが付けられます。</span><span class="sxs-lookup"><span data-stu-id="3e566-p103">The range of display levels is from -32,767 to +32,767. Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="3e566-113">バンド内の図形の Z オーダーを変更するには、次のコマンドを使用して[前方へ移動]、[後方に送信]、[前面に移動]、および [戻る **] を使用します**。</span><span class="sxs-lookup"><span data-stu-id="3e566-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="3e566-114">これらのコマンドが指定したバンドから図形を移動すると、セルが保護されていない限り、Microsoft Visio は図形の DisplayLevel セルに予約値 -32768 を表示します。</span><span class="sxs-lookup"><span data-stu-id="3e566-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="3e566-115">その場合、図形を別のバンドに移動することはできません。Visio では、"Shape protection and/layer properties" という警告が表示され、このコマンドが完全に実行されません。</span><span class="sxs-lookup"><span data-stu-id="3e566-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="3e566-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DisplayLevel] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3e566-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e566-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="3e566-117">Cell name:</span></span>  <br/> |<span data-ttu-id="3e566-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="3e566-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="3e566-119">プログラムから、インデックスによって [DisplayLevel] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e566-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e566-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3e566-120">Section index:</span></span>  <br/> |<span data-ttu-id="3e566-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3e566-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3e566-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3e566-122">Row index:</span></span>  <br/> |<span data-ttu-id="3e566-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="3e566-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="3e566-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3e566-124">Cell index:</span></span>  <br/> |<span data-ttu-id="3e566-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="3e566-125">**visSLODisplayLevel**</span></span> <br/> |
   

