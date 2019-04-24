---
title: '[ConLineJumpDirY] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: 図形に接続する垂直方向の動的コネクタに表示される飛び越し点の向きを指定します。
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342743"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="ef36e-103">[ConLineJumpDirY] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="ef36e-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ef36e-104">図形に接続する垂直方向の動的コネクタに表示される飛び越し点の向きを指定します。</span><span class="sxs-lookup"><span data-stu-id="ef36e-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="ef36e-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ef36e-105">**Value**</span></span>|<span data-ttu-id="ef36e-106">**飛び越し点の方向**</span><span class="sxs-lookup"><span data-stu-id="ef36e-106">**Line Jump Direction**</span></span>|<span data-ttu-id="ef36e-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="ef36e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ef36e-108">.0</span><span class="sxs-lookup"><span data-stu-id="ef36e-108">0</span></span>  <br/> | <span data-ttu-id="ef36e-109">ページの既定値</span><span class="sxs-lookup"><span data-stu-id="ef36e-109">Page default</span></span>  <br/> |<span data-ttu-id="ef36e-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="ef36e-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="ef36e-111">1-d</span><span class="sxs-lookup"><span data-stu-id="ef36e-111">1</span></span>  <br/> | <span data-ttu-id="ef36e-112">左</span><span class="sxs-lookup"><span data-stu-id="ef36e-112">Left</span></span>  <br/> |<span data-ttu-id="ef36e-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="ef36e-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="ef36e-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="ef36e-114">2</span></span>  <br/> | <span data-ttu-id="ef36e-115">右</span><span class="sxs-lookup"><span data-stu-id="ef36e-115">Right</span></span>  <br/> |<span data-ttu-id="ef36e-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="ef36e-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef36e-117">解説</span><span class="sxs-lookup"><span data-stu-id="ef36e-117">Remarks</span></span>

<span data-ttu-id="ef36e-118">ページ上の*すべて*のコネクタジャンプの既定の垂直方向を設定するには、[ページレイアウト] セクションの [[pagelinejumpdiry]] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="ef36e-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="ef36e-119">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpDirY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ef36e-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ef36e-120">セル名:</span><span class="sxs-lookup"><span data-stu-id="ef36e-120">Cell name:</span></span>  <br/> | <span data-ttu-id="ef36e-121">[conlinejumpdiry]</span><span class="sxs-lookup"><span data-stu-id="ef36e-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="ef36e-122">プログラムから、インデックスによって [ConLineJumpDirY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ef36e-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ef36e-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ef36e-123">Section index:</span></span>  <br/> |<span data-ttu-id="ef36e-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ef36e-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ef36e-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ef36e-125">Row index:</span></span>  <br/> |<span data-ttu-id="ef36e-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ef36e-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="ef36e-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ef36e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="ef36e-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="ef36e-128">**visSLOJumpDirY**</span></span> <br/> |
   

