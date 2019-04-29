---
title: '[WalkPreference] セル ([Glue Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: 1-D 図形をあいまいな位置に移動したときに、その図形の端点が、動的接着によって接着先の図形にある水平方向の接続ポイントに移動するのか、または垂直方向の接続ポイントに移動するのかを指定します。既定では、1-D 図形の始点と終点の両方とも水平方向の接続ポイントに移動します。
ms.openlocfilehash: 05f7ded3f7336dc2f8598e8d1e9edc501b511546
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408608"
---
# <a name="walkpreference-cell-glue-info-section"></a><span data-ttu-id="4c183-104">[WalkPreference] セル ([Glue Info] セクション)</span><span class="sxs-lookup"><span data-stu-id="4c183-104">WalkPreference Cell (Glue Info Section)</span></span>

<span data-ttu-id="4c183-p102">1-D 図形をあいまいな位置に移動したときに、その図形の端点が、動的接着によって接着先の図形にある水平方向の接続ポイントに移動するのか、または垂直方向の接続ポイントに移動するのかを指定します。既定では、1-D 図形の始点と終点の両方とも水平方向の接続ポイントに移動します。</span><span class="sxs-lookup"><span data-stu-id="4c183-p102">Determines whether an endpoint of a 1-D shape moves to a horizontal or vertical connection point on the shape it is glued to, using dynamic glue, when the shape is moved to an ambiguous position. By default, both endpoints of the 1-D shape move to horizontal connection points.</span></span>
  
|<span data-ttu-id="4c183-107">**値**</span><span class="sxs-lookup"><span data-stu-id="4c183-107">**Value**</span></span>|<span data-ttu-id="4c183-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="4c183-108">**Description**</span></span>|<span data-ttu-id="4c183-109">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="4c183-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4c183-110">1 </span><span class="sxs-lookup"><span data-stu-id="4c183-110">1</span></span>  <br/> | <span data-ttu-id="4c183-111">1-D 図形の始点は垂直方向の接続ポイントに移動し、終点は水平方向の接続ポイントに移動します (上から横または下から横の接続)。</span><span class="sxs-lookup"><span data-stu-id="4c183-111">The begin point of the 1-D shape moves to a vertical connection point, and the endpoint moves to a horizontal connection point (top-to-side or bottom-to-side connections).</span></span>  <br/> |<span data-ttu-id="4c183-112">**visWalkPrefBegNS**</span><span class="sxs-lookup"><span data-stu-id="4c183-112">**visWalkPrefBegNS**</span></span> <br/> |
| <span data-ttu-id="4c183-113">2 </span><span class="sxs-lookup"><span data-stu-id="4c183-113">2</span></span>  <br/> | <span data-ttu-id="4c183-114">1-D 図形の始点は水平方向の接続ポイントに移動し、終点は垂直方向の接続ポイントに移動します (横から上または横から下の接続)。</span><span class="sxs-lookup"><span data-stu-id="4c183-114">The begin point of the 1-D shape moves to a horizontal connection point, and the endpoint moves to a vertical connection point (side-to-top or side-to-bottom connections).</span></span>  <br/> |<span data-ttu-id="4c183-115">**visWalkPrefEndNS**</span><span class="sxs-lookup"><span data-stu-id="4c183-115">**visWalkPrefEndNS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c183-116">注釈</span><span class="sxs-lookup"><span data-stu-id="4c183-116">Remarks</span></span>

<span data-ttu-id="4c183-p103">このセルは、動的コネクタには影響を与えません。動的コネクタの動作は、その迂回方法によって決まります。ページ上のすべての動的コネクタに対する既定の迂回方法については [RouteStyle] セルを、特定の動的コネクタの迂回方法については [ShapeRouteStyle] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c183-p103">This cell has no effect on dynamic connectors. A dynamic connector's behavior is determined by its routing style. See the RouteStyle cell for the default routing style for dynamic connectors on a page, or the ShapeRouteStyle for the routing style of a particular dynamic connector.</span></span>
  
<span data-ttu-id="4c183-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [WalkPreference] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4c183-120">To get a reference to the WalkPreference cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c183-121">セル名 :</span><span class="sxs-lookup"><span data-stu-id="4c183-121">Cell name:</span></span>  <br/> | <span data-ttu-id="4c183-122">[walkpreference]</span><span class="sxs-lookup"><span data-stu-id="4c183-122">WalkPreference</span></span>  <br/> |
   
<span data-ttu-id="4c183-123">プログラムから、インデックスによって [WalkPreference] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4c183-123">To get a reference to the WalkPreference cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c183-124">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4c183-124">Section index:</span></span>  <br/> |<span data-ttu-id="4c183-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4c183-125">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4c183-126">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4c183-126">Row index:</span></span>  <br/> |<span data-ttu-id="4c183-127">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="4c183-127">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="4c183-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4c183-128">Cell index:</span></span>  <br/> |<span data-ttu-id="4c183-129">**visWalkPref**</span><span class="sxs-lookup"><span data-stu-id="4c183-129">**visWalkPref**</span></span> <br/> |
   

