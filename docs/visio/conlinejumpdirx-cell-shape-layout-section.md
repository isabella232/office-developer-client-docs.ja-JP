---
title: '[ConLineJumpDirX] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: 図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342750"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="18a64-103">[ConLineJumpDirX] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="18a64-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="18a64-104">図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。</span><span class="sxs-lookup"><span data-stu-id="18a64-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="18a64-105">**値**</span><span class="sxs-lookup"><span data-stu-id="18a64-105">**Value**</span></span>|<span data-ttu-id="18a64-106">**飛び越し点の方向**</span><span class="sxs-lookup"><span data-stu-id="18a64-106">**Line jump direction**</span></span>|<span data-ttu-id="18a64-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="18a64-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="18a64-108">.0</span><span class="sxs-lookup"><span data-stu-id="18a64-108">0</span></span>  <br/> | <span data-ttu-id="18a64-109">ページの既定値</span><span class="sxs-lookup"><span data-stu-id="18a64-109">Page default</span></span>  <br/> |<span data-ttu-id="18a64-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="18a64-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="18a64-111">1-d</span><span class="sxs-lookup"><span data-stu-id="18a64-111">1</span></span>  <br/> | <span data-ttu-id="18a64-112">上</span><span class="sxs-lookup"><span data-stu-id="18a64-112">Up</span></span>  <br/> |<span data-ttu-id="18a64-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="18a64-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="18a64-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="18a64-114">2</span></span>  <br/> | <span data-ttu-id="18a64-115">下へ</span><span class="sxs-lookup"><span data-stu-id="18a64-115">Down</span></span>  <br/> |<span data-ttu-id="18a64-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="18a64-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18a64-117">解説</span><span class="sxs-lookup"><span data-stu-id="18a64-117">Remarks</span></span>

<span data-ttu-id="18a64-118">ページ上の*すべて*のコネクタジャンプの既定の水平方向を設定するには、[ページレイアウト] セクションの [[pagelinejumpdirx]] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="18a64-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="18a64-119">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpDirX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="18a64-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18a64-120">セル名:</span><span class="sxs-lookup"><span data-stu-id="18a64-120">Cell name:</span></span>  <br/> | <span data-ttu-id="18a64-121">[conlinejumpdirx]</span><span class="sxs-lookup"><span data-stu-id="18a64-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="18a64-122">プログラムから、インデックスによって [ConLineJumpDirX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="18a64-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18a64-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="18a64-123">Section index:</span></span>  <br/> |<span data-ttu-id="18a64-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18a64-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="18a64-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="18a64-125">Row index:</span></span>  <br/> |<span data-ttu-id="18a64-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="18a64-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="18a64-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="18a64-127">Cell index:</span></span>  <br/> |<span data-ttu-id="18a64-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="18a64-128">**visSLOJumpDirX**</span></span> <br/> |
   

