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
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431009"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="63992-103">[PageLineJumpDirX] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="63992-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="63992-104">図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。</span><span class="sxs-lookup"><span data-stu-id="63992-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="63992-105">**値**</span><span class="sxs-lookup"><span data-stu-id="63992-105">**Value**</span></span>|<span data-ttu-id="63992-106">**飛び越し点の方向**</span><span class="sxs-lookup"><span data-stu-id="63992-106">**Line jump direction**</span></span>|<span data-ttu-id="63992-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="63992-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="63992-108">.0</span><span class="sxs-lookup"><span data-stu-id="63992-108">0</span></span>  <br/> | <span data-ttu-id="63992-109">既定値です。左、またはページの設定に従います。</span><span class="sxs-lookup"><span data-stu-id="63992-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="63992-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="63992-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="63992-111">1 </span><span class="sxs-lookup"><span data-stu-id="63992-111">1</span></span>  <br/> | <span data-ttu-id="63992-112">上</span><span class="sxs-lookup"><span data-stu-id="63992-112">Up</span></span>  <br/> |<span data-ttu-id="63992-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="63992-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="63992-114">2 </span><span class="sxs-lookup"><span data-stu-id="63992-114">2</span></span>  <br/> | <span data-ttu-id="63992-115">下へ</span><span class="sxs-lookup"><span data-stu-id="63992-115">Down</span></span>  <br/> |<span data-ttu-id="63992-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="63992-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63992-117">注釈</span><span class="sxs-lookup"><span data-stu-id="63992-117">Remarks</span></span>

<span data-ttu-id="63992-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前による [PageLineJumpDirX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="63992-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="63992-119">セル名 :</span><span class="sxs-lookup"><span data-stu-id="63992-119">Cell name:</span></span>  <br/> | <span data-ttu-id="63992-120">[pagelinejumpdirx]</span><span class="sxs-lookup"><span data-stu-id="63992-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="63992-121">プログラムから、インデックスによる [PageLineJumpDirX] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="63992-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="63992-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="63992-122">Section index:</span></span>  <br/> |<span data-ttu-id="63992-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="63992-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="63992-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="63992-124">Row index:</span></span>  <br/> |<span data-ttu-id="63992-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="63992-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="63992-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="63992-126">Cell index:</span></span>  <br/> |<span data-ttu-id="63992-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="63992-127">**visPLOJumpDirX**</span></span> <br/> |
   

