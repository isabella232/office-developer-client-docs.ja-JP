---
title: '[PageLineJumpDirY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: 図面ページ上にある垂直方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329898"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="fcd9d-103">[PageLineJumpDirY] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="fcd9d-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="fcd9d-104">図面ページ上にある垂直方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。</span><span class="sxs-lookup"><span data-stu-id="fcd9d-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="fcd9d-105">**値**</span><span class="sxs-lookup"><span data-stu-id="fcd9d-105">**Value**</span></span>|<span data-ttu-id="fcd9d-106">**飛び越し点の方向**</span><span class="sxs-lookup"><span data-stu-id="fcd9d-106">**Line jump direction**</span></span>|<span data-ttu-id="fcd9d-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="fcd9d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="fcd9d-108">.0</span><span class="sxs-lookup"><span data-stu-id="fcd9d-108">0</span></span>  <br/> | <span data-ttu-id="fcd9d-109">既定値です。上、またはページの設定に従います。</span><span class="sxs-lookup"><span data-stu-id="fcd9d-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="fcd9d-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="fcd9d-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="fcd9d-111">1-d</span><span class="sxs-lookup"><span data-stu-id="fcd9d-111">1</span></span>  <br/> | <span data-ttu-id="fcd9d-112">左</span><span class="sxs-lookup"><span data-stu-id="fcd9d-112">Left</span></span>  <br/> |<span data-ttu-id="fcd9d-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="fcd9d-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="fcd9d-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="fcd9d-114">2</span></span>  <br/> | <span data-ttu-id="fcd9d-115">右</span><span class="sxs-lookup"><span data-stu-id="fcd9d-115">Right</span></span>  <br/> |<span data-ttu-id="fcd9d-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="fcd9d-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcd9d-117">解説</span><span class="sxs-lookup"><span data-stu-id="fcd9d-117">Remarks</span></span>

<span data-ttu-id="fcd9d-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前による [PageLineJumpDirY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fcd9d-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fcd9d-119">セル名 :</span><span class="sxs-lookup"><span data-stu-id="fcd9d-119">Cell name:</span></span>  <br/> | <span data-ttu-id="fcd9d-120">[pagelinejumpdiry]</span><span class="sxs-lookup"><span data-stu-id="fcd9d-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="fcd9d-121">プログラムから、インデックスによる [PageLineJumpDirY] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fcd9d-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fcd9d-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fcd9d-122">Section index:</span></span>  <br/> |<span data-ttu-id="fcd9d-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fcd9d-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fcd9d-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fcd9d-124">Row index:</span></span>  <br/> |<span data-ttu-id="fcd9d-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="fcd9d-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="fcd9d-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fcd9d-126">Cell index:</span></span>  <br/> |<span data-ttu-id="fcd9d-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="fcd9d-127">**visPLOJumpDirY**</span></span> <br/> |
   

