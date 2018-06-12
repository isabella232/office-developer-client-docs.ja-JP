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
ms.openlocfilehash: a87ba7451d73af50de4a110ecdc12b3e23e14d5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805141"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="4baec-104">[CtrlAsInput] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="4baec-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="4baec-p102">コントロール ハンドルを使用して図形を操作するときに、どの図形を親図形にするかを指定します。このセルの値は、図面ページ上にあるすべての図形の動作に適用されます。</span><span class="sxs-lookup"><span data-stu-id="4baec-p102">Determines which shape is the parent when using shapes with control handles. This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="4baec-107">**値**</span><span class="sxs-lookup"><span data-stu-id="4baec-107">**Value**</span></span>|<span data-ttu-id="4baec-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="4baec-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4baec-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="4baec-109">TRUE</span></span>  <br/> | <span data-ttu-id="4baec-110">コントロール ハンドルの接続先になっている図形を親にします。</span><span class="sxs-lookup"><span data-stu-id="4baec-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="4baec-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="4baec-111">FALSE</span></span>  <br/> | <span data-ttu-id="4baec-p103">既定値です。コントロール ハンドルを含んでいる図形を親にします。</span><span class="sxs-lookup"><span data-stu-id="4baec-p103">The default. Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4baec-114">備考</span><span class="sxs-lookup"><span data-stu-id="4baec-114">Remarks</span></span>

<span data-ttu-id="4baec-115">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[CtrlAsInput] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4baec-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4baec-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="4baec-116">Cell name:</span></span>  <br/> | <span data-ttu-id="4baec-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="4baec-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="4baec-118">プログラムから、インデックスによって [CtrlAsInput] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4baec-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4baec-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4baec-119">Section index:</span></span>  <br/> |<span data-ttu-id="4baec-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4baec-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4baec-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4baec-121">Row index:</span></span>  <br/> |<span data-ttu-id="4baec-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="4baec-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="4baec-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4baec-123">Cell index:</span></span>  <br/> |<span data-ttu-id="4baec-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="4baec-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

