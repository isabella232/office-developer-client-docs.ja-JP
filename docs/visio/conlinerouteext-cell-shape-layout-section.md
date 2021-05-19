---
title: '[ConLineRouteExt] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: コネクタの外観を指定します。
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434614"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="ea95f-103">[ConLineRouteExt] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="ea95f-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ea95f-104">コネクタの外観を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea95f-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="ea95f-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ea95f-105">**Value**</span></span>|<span data-ttu-id="ea95f-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea95f-106">**Description**</span></span>|<span data-ttu-id="ea95f-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="ea95f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ea95f-108">0</span><span class="sxs-lookup"><span data-stu-id="ea95f-108">0</span></span>  <br/> | <span data-ttu-id="ea95f-109">既定値です。ページの設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="ea95f-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="ea95f-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="ea95f-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="ea95f-111">1</span><span class="sxs-lookup"><span data-stu-id="ea95f-111">1</span></span>  <br/> | <span data-ttu-id="ea95f-112">ストレート</span><span class="sxs-lookup"><span data-stu-id="ea95f-112">Straight</span></span>  <br/> |<span data-ttu-id="ea95f-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="ea95f-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="ea95f-114">2</span><span class="sxs-lookup"><span data-stu-id="ea95f-114">2</span></span>  <br/> | <span data-ttu-id="ea95f-115">曲線</span><span class="sxs-lookup"><span data-stu-id="ea95f-115">Curved</span></span>  <br/> |<span data-ttu-id="ea95f-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="ea95f-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea95f-117">注釈</span><span class="sxs-lookup"><span data-stu-id="ea95f-117">Remarks</span></span>

<span data-ttu-id="ea95f-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineRouteExt] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ea95f-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea95f-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="ea95f-119">Cell name:</span></span>  <br/> | <span data-ttu-id="ea95f-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="ea95f-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="ea95f-121">プログラムから、インデックスによって [ConLineRouteExt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea95f-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea95f-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea95f-122">Section index:</span></span>  <br/> |<span data-ttu-id="ea95f-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ea95f-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ea95f-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea95f-124">Row index:</span></span>  <br/> |<span data-ttu-id="ea95f-125">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ea95f-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="ea95f-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea95f-126">Cell index:</span></span>  <br/> |<span data-ttu-id="ea95f-127">**visSLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="ea95f-127">**visSLOLineRouteExt**</span></span> <br/> |
   

