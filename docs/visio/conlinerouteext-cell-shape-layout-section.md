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
ms.openlocfilehash: 7724466b6ad225fcf39243bc80ba2e440f3b700b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805087"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="d973f-103">[ConLineRouteExt] セル ([図形レイアウト] セクション)</span><span class="sxs-lookup"><span data-stu-id="d973f-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="d973f-104">コネクタの外観を指定します。</span><span class="sxs-lookup"><span data-stu-id="d973f-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="d973f-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d973f-105">**Value**</span></span>|<span data-ttu-id="d973f-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d973f-106">**Description**</span></span>|<span data-ttu-id="d973f-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="d973f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d973f-108">0</span><span class="sxs-lookup"><span data-stu-id="d973f-108">0</span></span>  <br/> | <span data-ttu-id="d973f-109">既定値です。ページの設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="d973f-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="d973f-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="d973f-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="d973f-111">1</span><span class="sxs-lookup"><span data-stu-id="d973f-111">1</span></span>  <br/> | <span data-ttu-id="d973f-112">直線</span><span class="sxs-lookup"><span data-stu-id="d973f-112">Straight</span></span>  <br/> |<span data-ttu-id="d973f-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="d973f-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="d973f-114">2</span><span class="sxs-lookup"><span data-stu-id="d973f-114">2</span></span>  <br/> | <span data-ttu-id="d973f-115">曲線</span><span class="sxs-lookup"><span data-stu-id="d973f-115">Curved</span></span>  <br/> |<span data-ttu-id="d973f-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="d973f-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d973f-117">注釈</span><span class="sxs-lookup"><span data-stu-id="d973f-117">Remarks</span></span>

<span data-ttu-id="d973f-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineRouteExt] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d973f-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d973f-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="d973f-119">Cell name:</span></span>  <br/> | <span data-ttu-id="d973f-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="d973f-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="d973f-121">プログラムから、インデックスによって [ConLineRouteExt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d973f-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d973f-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d973f-122">Section index:</span></span>  <br/> |<span data-ttu-id="d973f-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d973f-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d973f-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d973f-124">Row index:</span></span>  <br/> |<span data-ttu-id="d973f-125">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="d973f-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="d973f-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d973f-126">Cell index:</span></span>  <br/> |<span data-ttu-id="d973f-127">**visSLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="d973f-127">**visSLOLineRouteExt**</span></span> <br/> |
   

