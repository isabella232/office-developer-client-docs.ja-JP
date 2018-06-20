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
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805069"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="6db9e-103">[ConLineJumpDirY] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="6db9e-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="6db9e-104">図形に接続する垂直方向の動的コネクタに表示される飛び越し点の向きを指定します。</span><span class="sxs-lookup"><span data-stu-id="6db9e-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="6db9e-105">**値**</span><span class="sxs-lookup"><span data-stu-id="6db9e-105">**Value**</span></span>|<span data-ttu-id="6db9e-106">**線の飛び越し点の方向**</span><span class="sxs-lookup"><span data-stu-id="6db9e-106">**Line Jump Direction**</span></span>|<span data-ttu-id="6db9e-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="6db9e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6db9e-108">0</span><span class="sxs-lookup"><span data-stu-id="6db9e-108">0</span></span>  <br/> | <span data-ttu-id="6db9e-109">ページの既定値</span><span class="sxs-lookup"><span data-stu-id="6db9e-109">Page default</span></span>  <br/> |<span data-ttu-id="6db9e-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="6db9e-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="6db9e-111">1</span><span class="sxs-lookup"><span data-stu-id="6db9e-111">1</span></span>  <br/> | <span data-ttu-id="6db9e-112">左</span><span class="sxs-lookup"><span data-stu-id="6db9e-112">Left</span></span>  <br/> |<span data-ttu-id="6db9e-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="6db9e-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="6db9e-114">2</span><span class="sxs-lookup"><span data-stu-id="6db9e-114">2</span></span>  <br/> | <span data-ttu-id="6db9e-115">右</span><span class="sxs-lookup"><span data-stu-id="6db9e-115">Right</span></span>  <br/> |<span data-ttu-id="6db9e-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="6db9e-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6db9e-117">備考</span><span class="sxs-lookup"><span data-stu-id="6db9e-117">Remarks</span></span>

<span data-ttu-id="6db9e-118">ページにジャンプする*すべて*のコネクタの垂直方向の既定値を設定するのには、PageLineJumpDirY セルを使用して、「ページ レイアウト」セクションでします。</span><span class="sxs-lookup"><span data-stu-id="6db9e-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="6db9e-119">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ConLineJumpDirY] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="6db9e-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6db9e-120">セル名:</span><span class="sxs-lookup"><span data-stu-id="6db9e-120">Cell name:</span></span>  <br/> | <span data-ttu-id="6db9e-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="6db9e-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="6db9e-122">プログラムから、インデックスによって [ConLineJumpDirY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6db9e-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6db9e-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6db9e-123">Section index:</span></span>  <br/> |<span data-ttu-id="6db9e-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6db9e-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6db9e-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6db9e-125">Row index:</span></span>  <br/> |<span data-ttu-id="6db9e-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="6db9e-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="6db9e-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6db9e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="6db9e-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="6db9e-128">**visSLOJumpDirY**</span></span> <br/> |
   

