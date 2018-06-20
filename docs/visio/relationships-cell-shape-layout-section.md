---
title: '[Relationships] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: コンテナー、リスト、引き出し、および図形どうしの関係を格納します。
ms.openlocfilehash: c3410ad15581ff1704d7a43dd7ed5fa193f668b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806184"
---
# <a name="relationships-cell-shape-layout-section"></a><span data-ttu-id="33fae-103">[Relationships] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="33fae-103">Relationships Cell (Shape Layout Section)</span></span>

<span data-ttu-id="33fae-104">コンテナー、リスト、引き出し、および図形どうしの関係を格納します。</span><span class="sxs-lookup"><span data-stu-id="33fae-104">Stores the relationships between containers, lists, callouts, and shapes.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="33fae-105">注釈</span><span class="sxs-lookup"><span data-stu-id="33fae-105">Remarks</span></span>

 <span data-ttu-id="33fae-106">Microsoft Visio では、この図形に関連するリレーションシップを保存するのには関係のセルを使用します。</span><span class="sxs-lookup"><span data-stu-id="33fae-106">Microsoft Visio uses the Relationships cell to store the relationships that involve this shape.</span></span> <span data-ttu-id="33fae-107">DEPENDSON 関数は、表示されているパラメーターを使用して一連は、次の表に示すように、この図形では、リレーションシップを表現する使用されます。</span><span class="sxs-lookup"><span data-stu-id="33fae-107">A series of DEPENDSON functions, with the parameters shown, are used to represent relationships with this shape, as shown in the following table.</span></span> 
  
|<span data-ttu-id="33fae-108">**最初のパラメーター**</span><span class="sxs-lookup"><span data-stu-id="33fae-108">**First parameter**</span></span>|<span data-ttu-id="33fae-109">**追加のパラメーター**</span><span class="sxs-lookup"><span data-stu-id="33fae-109">**Additional parameters**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33fae-110">1</span><span class="sxs-lookup"><span data-stu-id="33fae-110">1</span></span>  <br/> |<span data-ttu-id="33fae-111">このコンテナーのメンバーである図形。</span><span class="sxs-lookup"><span data-stu-id="33fae-111">Shapes that are members of this container.</span></span>  <br/> |
|<span data-ttu-id="33fae-112">2</span><span class="sxs-lookup"><span data-stu-id="33fae-112">2</span></span>  <br/> |<span data-ttu-id="33fae-113">このリストのメンバーである図形。</span><span class="sxs-lookup"><span data-stu-id="33fae-113">Shapes that are members of this list.</span></span>  <br/> |
|<span data-ttu-id="33fae-114">3</span><span class="sxs-lookup"><span data-stu-id="33fae-114">3</span></span>  <br/> |<span data-ttu-id="33fae-115">この図形に関連付けられた引き出し。</span><span class="sxs-lookup"><span data-stu-id="33fae-115">Callouts that are associated with this shape.</span></span>  <br/> |
|<span data-ttu-id="33fae-116">4</span><span class="sxs-lookup"><span data-stu-id="33fae-116">4</span></span>  <br/> |<span data-ttu-id="33fae-117">この図形がメンバーとして属しているコンテナー。</span><span class="sxs-lookup"><span data-stu-id="33fae-117">Containers that this shape is a member of.</span></span>  <br/> |
|<span data-ttu-id="33fae-118">5</span><span class="sxs-lookup"><span data-stu-id="33fae-118">5</span></span>  <br/> |<span data-ttu-id="33fae-119">このリスト項目がメンバーとして属しているリスト。</span><span class="sxs-lookup"><span data-stu-id="33fae-119">List that this list item is a member of.</span></span>  <br/> |
|<span data-ttu-id="33fae-120">6</span><span class="sxs-lookup"><span data-stu-id="33fae-120">6</span></span>  <br/> |<span data-ttu-id="33fae-121">この引き出しに関連付けられた図形。</span><span class="sxs-lookup"><span data-stu-id="33fae-121">Shape associated with this callout.</span></span>  <br/> |
|<span data-ttu-id="33fae-122">7</span><span class="sxs-lookup"><span data-stu-id="33fae-122">7</span></span>  <br/> |<span data-ttu-id="33fae-123">この図形が配置されている左端のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="33fae-123">Container on the left boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="33fae-124">8</span><span class="sxs-lookup"><span data-stu-id="33fae-124">8</span></span>  <br/> |<span data-ttu-id="33fae-125">この図形が配置されている右端のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="33fae-125">Container on the right boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="33fae-126">9</span><span class="sxs-lookup"><span data-stu-id="33fae-126">9</span></span>  <br/> |<span data-ttu-id="33fae-127">この図形が配置されている上端のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="33fae-127">Container on the top boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="33fae-128">10</span><span class="sxs-lookup"><span data-stu-id="33fae-128">10</span></span>  <br/> |<span data-ttu-id="33fae-129">この図形が配置されている下端のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="33fae-129">Container on the bottom boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="33fae-130">11</span><span class="sxs-lookup"><span data-stu-id="33fae-130">11</span></span>  <br/> |<span data-ttu-id="33fae-131">このリストが重なっているリスト。</span><span class="sxs-lookup"><span data-stu-id="33fae-131">List that this list overlaps.</span></span>  <br/> |
   
<span data-ttu-id="33fae-132">参照を取得する関係のセルに名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="33fae-132">To get a reference to the Relationships cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33fae-133">セル名:</span><span class="sxs-lookup"><span data-stu-id="33fae-133">Cell name:</span></span>  <br/> |<span data-ttu-id="33fae-134">Relationships</span><span class="sxs-lookup"><span data-stu-id="33fae-134">Relationships</span></span>  <br/> |
   
<span data-ttu-id="33fae-135">プログラムから、インデックスによって [リレーションシップ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="33fae-135">To get a reference to the Relationships cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33fae-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="33fae-136">Section index:</span></span>  <br/> |<span data-ttu-id="33fae-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="33fae-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="33fae-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="33fae-138">Row index:</span></span>  <br/> |<span data-ttu-id="33fae-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="33fae-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="33fae-140">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="33fae-140">Cell index:</span></span>  <br/> |<span data-ttu-id="33fae-141">**visSLORelationships**</span><span class="sxs-lookup"><span data-stu-id="33fae-141">**visSLORelationships**</span></span> <br/> |
   

