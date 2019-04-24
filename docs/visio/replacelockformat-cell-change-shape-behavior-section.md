---
title: '[ReplaceLockFormat] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。 マスター シェイプの [ReplaceLockFormat] セルが TRUE (1) に設定されている場合、マスターの書式設定値は、マスターによって置き換えられる図形の対応する値すべてに優先します。
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329891"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="772d6-104">[ReplaceLockFormat] セル ([図形の動作の変更] セクション)</span><span class="sxs-lookup"><span data-stu-id="772d6-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="772d6-105">マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="772d6-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="772d6-106">マスター シェイプの [**ReplaceLockFormat**] セルが TRUE (1) に設定されている場合、マスターの書式設定値は、マスターによって置き換えられる図形の対応する値すべてに優先します。</span><span class="sxs-lookup"><span data-stu-id="772d6-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="772d6-107">**値**</span><span class="sxs-lookup"><span data-stu-id="772d6-107">**Value**</span></span>|<span data-ttu-id="772d6-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="772d6-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="772d6-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="772d6-109">TRUE</span></span>  <br/> |<span data-ttu-id="772d6-110">マスター シェイプの [**ReplaceLockFormat**] セルが TRUE (1) に設定されている場合、マスターの書式設定値は、マスターによって置き換えられる図形の対応する値すべてに優先します。</span><span class="sxs-lookup"><span data-stu-id="772d6-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="772d6-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="772d6-111">FALSE</span></span>  <br/> |<span data-ttu-id="772d6-112">マスター シェイプの [**ReplaceLockFormat**] セルが FALSE に設定されている場合、置換後の図形には、置換操作の後、古い図形のローカルの書式設定値が格納されます。</span><span class="sxs-lookup"><span data-stu-id="772d6-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="772d6-113">解説</span><span class="sxs-lookup"><span data-stu-id="772d6-113">Remarks</span></span>

<span data-ttu-id="772d6-114">[**ReplaceLockFormat**] セルは、マスター シェイプが、図形の置換操作時に、次のセクション内のローカル書式設定値に優先するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="772d6-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="772d6-115">[**塗りつぶしの書式設定**] セクション</span><span class="sxs-lookup"><span data-stu-id="772d6-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="772d6-116">[**線の書式設定**] セクション</span><span class="sxs-lookup"><span data-stu-id="772d6-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="772d6-117">[**クイック スタイル**] セクション</span><span class="sxs-lookup"><span data-stu-id="772d6-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="772d6-118">[**テーマのプロパティ**] セクション</span><span class="sxs-lookup"><span data-stu-id="772d6-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="772d6-119">[**グラデーションのプロパティ**] セクション</span><span class="sxs-lookup"><span data-stu-id="772d6-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="772d6-120">[**ベベルのプロパティ**] セクション</span><span class="sxs-lookup"><span data-stu-id="772d6-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="772d6-121">[**追加効果のプロパティ**] セクション</span><span class="sxs-lookup"><span data-stu-id="772d6-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="772d6-122">[**線のグラデーションの分岐点**] セクション</span><span class="sxs-lookup"><span data-stu-id="772d6-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="772d6-123">[**塗りつぶしのグラデーションの分岐点**] セクション</span><span class="sxs-lookup"><span data-stu-id="772d6-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="772d6-124">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ReplaceLockFormat**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="772d6-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="772d6-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="772d6-125">Cell name:</span></span>  <br/> | <span data-ttu-id="772d6-126">[replacelockformat]</span><span class="sxs-lookup"><span data-stu-id="772d6-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="772d6-127">プログラムから、インデックスによって [**ReplaceLockFormat**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="772d6-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="772d6-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="772d6-128">Section index:</span></span>  <br/> |<span data-ttu-id="772d6-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="772d6-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="772d6-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="772d6-130">Row index:</span></span>  <br/> |<span data-ttu-id="772d6-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="772d6-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="772d6-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="772d6-132">Cell index:</span></span>  <br/> |<span data-ttu-id="772d6-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="772d6-133">**visReplaceLockFormat**</span></span> <br/> |
   

