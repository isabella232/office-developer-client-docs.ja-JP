---
title: '[PageLineJumpDirX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: 図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805961"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="9d933-103">[PageLineJumpDirX] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="9d933-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="9d933-104">図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d933-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="9d933-105">**値**</span><span class="sxs-lookup"><span data-stu-id="9d933-105">**Value**</span></span>|<span data-ttu-id="9d933-106">**線の飛び越し点の方向**</span><span class="sxs-lookup"><span data-stu-id="9d933-106">**Line jump direction**</span></span>|<span data-ttu-id="9d933-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="9d933-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9d933-108">0</span><span class="sxs-lookup"><span data-stu-id="9d933-108">0</span></span>  <br/> | <span data-ttu-id="9d933-109">既定値です。左、またはページの設定に従います。</span><span class="sxs-lookup"><span data-stu-id="9d933-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="9d933-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="9d933-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="9d933-111">1</span><span class="sxs-lookup"><span data-stu-id="9d933-111">1</span></span>  <br/> | <span data-ttu-id="9d933-112">上</span><span class="sxs-lookup"><span data-stu-id="9d933-112">Up</span></span>  <br/> |<span data-ttu-id="9d933-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="9d933-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="9d933-114">2</span><span class="sxs-lookup"><span data-stu-id="9d933-114">2</span></span>  <br/> | <span data-ttu-id="9d933-115">下</span><span class="sxs-lookup"><span data-stu-id="9d933-115">Down</span></span>  <br/> |<span data-ttu-id="9d933-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="9d933-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d933-117">備考</span><span class="sxs-lookup"><span data-stu-id="9d933-117">Remarks</span></span>

<span data-ttu-id="9d933-118">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PageLineJumpDirX] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="9d933-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d933-119">セル名 :</span><span class="sxs-lookup"><span data-stu-id="9d933-119">Cell name:</span></span>  <br/> | <span data-ttu-id="9d933-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="9d933-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="9d933-121">プログラムから、インデックスによって [PageLineJumpDirX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9d933-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d933-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9d933-122">Section index:</span></span>  <br/> |<span data-ttu-id="9d933-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9d933-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9d933-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9d933-124">Row index:</span></span>  <br/> |<span data-ttu-id="9d933-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="9d933-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="9d933-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9d933-126">Cell index:</span></span>  <br/> |<span data-ttu-id="9d933-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="9d933-127">**visPLOJumpDirX**</span></span> <br/> |
   

