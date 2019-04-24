---
title: '[CtrlAsInput] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: コントロール ハンドルを使用して図形を操作するときに、どの図形を親図形にするかを指定します。このセルの値は、図面ページ上にあるすべての図形の動作に適用されます。
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282909"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="a6254-104">[CtrlAsInput] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="a6254-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="a6254-p102">コントロール ハンドルを使用して図形を操作するときに、どの図形を親図形にするかを指定します。このセルの値は、図面ページ上にあるすべての図形の動作に適用されます。</span><span class="sxs-lookup"><span data-stu-id="a6254-p102">Determines which shape is the parent when using shapes with control handles. This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="a6254-107">**値**</span><span class="sxs-lookup"><span data-stu-id="a6254-107">**Value**</span></span>|<span data-ttu-id="a6254-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="a6254-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a6254-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="a6254-109">TRUE</span></span>  <br/> | <span data-ttu-id="a6254-110">コントロール ハンドルの接続先になっている図形を親にします。</span><span class="sxs-lookup"><span data-stu-id="a6254-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="a6254-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="a6254-111">FALSE</span></span>  <br/> | <span data-ttu-id="a6254-p103">既定値です。コントロール ハンドルを含んでいる図形を親にします。</span><span class="sxs-lookup"><span data-stu-id="a6254-p103">The default. Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6254-114">解説</span><span class="sxs-lookup"><span data-stu-id="a6254-114">Remarks</span></span>

<span data-ttu-id="a6254-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [CtrlAsInput] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6254-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6254-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="a6254-116">Cell name:</span></span>  <br/> | <span data-ttu-id="a6254-117">[ctrlasinput]</span><span class="sxs-lookup"><span data-stu-id="a6254-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="a6254-118">プログラムから、インデックスによって [CtrlAsInput] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6254-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6254-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a6254-119">Section index:</span></span>  <br/> |<span data-ttu-id="a6254-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a6254-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a6254-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a6254-121">Row index:</span></span>  <br/> |<span data-ttu-id="a6254-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a6254-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="a6254-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a6254-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a6254-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="a6254-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

