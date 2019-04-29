---
title: '[PlaceDepth] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: レイアウトを作成する前に図面を分析する方法を指定します。また、レイアウトの種類も指定します。
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432038"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="43672-103">[PlaceDepth] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="43672-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="43672-104">レイアウトを作成する前に図面を分析する方法を指定します。また、レイアウトの種類も指定します。</span><span class="sxs-lookup"><span data-stu-id="43672-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="43672-105">**値**</span><span class="sxs-lookup"><span data-stu-id="43672-105">**Value**</span></span>|<span data-ttu-id="43672-106">**垂直および水平レイアウトの配置の深さ**</span><span class="sxs-lookup"><span data-stu-id="43672-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="43672-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="43672-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="43672-108">.0</span><span class="sxs-lookup"><span data-stu-id="43672-108">0</span></span>  <br/> | <span data-ttu-id="43672-109">ページの既定値</span><span class="sxs-lookup"><span data-stu-id="43672-109">Page default</span></span>  <br/> |<span data-ttu-id="43672-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="43672-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="43672-111">1 </span><span class="sxs-lookup"><span data-stu-id="43672-111">1</span></span>  <br/> | <span data-ttu-id="43672-112">中</span><span class="sxs-lookup"><span data-stu-id="43672-112">Medium</span></span>  <br/> |<span data-ttu-id="43672-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="43672-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="43672-114">2 </span><span class="sxs-lookup"><span data-stu-id="43672-114">2</span></span>  <br/> | <span data-ttu-id="43672-115">深い</span><span class="sxs-lookup"><span data-stu-id="43672-115">Deep</span></span>  <br/> |<span data-ttu-id="43672-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="43672-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="43672-117">3 </span><span class="sxs-lookup"><span data-stu-id="43672-117">3</span></span>  <br/> | <span data-ttu-id="43672-118">浅い</span><span class="sxs-lookup"><span data-stu-id="43672-118">Shallow</span></span>  <br/> |<span data-ttu-id="43672-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="43672-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43672-120">注釈</span><span class="sxs-lookup"><span data-stu-id="43672-120">Remarks</span></span>

<span data-ttu-id="43672-121">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PlaceDepth] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="43672-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="43672-122">セル名:</span><span class="sxs-lookup"><span data-stu-id="43672-122">Cell name:</span></span>  <br/> | <span data-ttu-id="43672-123">[placedepth]</span><span class="sxs-lookup"><span data-stu-id="43672-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="43672-124">プログラムから、インデックスによって [PlaceDepth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="43672-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="43672-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="43672-125">Section index:</span></span>  <br/> |<span data-ttu-id="43672-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="43672-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="43672-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="43672-127">Row index:</span></span>  <br/> |<span data-ttu-id="43672-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="43672-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="43672-129">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="43672-129">Cell index:</span></span>  <br/> |<span data-ttu-id="43672-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="43672-130">**visPLOPlaceDepth**</span></span> <br/> |
   

