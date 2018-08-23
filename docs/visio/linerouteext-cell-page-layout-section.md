---
title: '[LineRouteExt] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: 図面ページにあるすべてのコネクタの既定の外観を指定します。
ms.openlocfilehash: 21da283f2d9ab43837b8fe4127840e89ea9d9949
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805724"
---
# <a name="linerouteext-cell-page-layout-section"></a><span data-ttu-id="e4279-103">[LineRouteExt] セル ([ページ レイアウト] セクション)</span><span class="sxs-lookup"><span data-stu-id="e4279-103">LineRouteExt Cell (Page Layout Section)</span></span>

<span data-ttu-id="e4279-104">図面ページにあるすべてのコネクタの既定の外観を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4279-104">Determines the default appearance for all connectors on a drawing page.</span></span>
  
|<span data-ttu-id="e4279-105">**値**</span><span class="sxs-lookup"><span data-stu-id="e4279-105">**Value**</span></span>|<span data-ttu-id="e4279-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="e4279-106">**Description**</span></span>|<span data-ttu-id="e4279-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="e4279-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e4279-108">0</span><span class="sxs-lookup"><span data-stu-id="e4279-108">0</span></span>  <br/> | <span data-ttu-id="e4279-109">既定値 (直線)</span><span class="sxs-lookup"><span data-stu-id="e4279-109">Default (straight)</span></span>  <br/> |<span data-ttu-id="e4279-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="e4279-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="e4279-111">1</span><span class="sxs-lookup"><span data-stu-id="e4279-111">1</span></span>  <br/> | <span data-ttu-id="e4279-112">直線</span><span class="sxs-lookup"><span data-stu-id="e4279-112">Straight</span></span>  <br/> |<span data-ttu-id="e4279-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="e4279-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="e4279-114">2</span><span class="sxs-lookup"><span data-stu-id="e4279-114">2</span></span>  <br/> | <span data-ttu-id="e4279-115">曲線</span><span class="sxs-lookup"><span data-stu-id="e4279-115">Curved</span></span>  <br/> |<span data-ttu-id="e4279-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="e4279-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4279-117">注釈</span><span class="sxs-lookup"><span data-stu-id="e4279-117">Remarks</span></span>

<span data-ttu-id="e4279-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineRouteExt] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e4279-118">To get a reference to the LineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e4279-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="e4279-119">Cell name:</span></span>  <br/> | <span data-ttu-id="e4279-120">LineRouteExt</span><span class="sxs-lookup"><span data-stu-id="e4279-120">LineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="e4279-121">プログラムから、インデックスによって [LineRouteExt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4279-121">To get a reference to the LineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e4279-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e4279-122">Section index:</span></span>  <br/> |<span data-ttu-id="e4279-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e4279-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e4279-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e4279-124">Row index:</span></span>  <br/> |<span data-ttu-id="e4279-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e4279-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="e4279-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e4279-126">Cell index:</span></span>  <br/> |<span data-ttu-id="e4279-127">**visPLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="e4279-127">**visPLOLineRouteExt**</span></span> <br/> |
   

