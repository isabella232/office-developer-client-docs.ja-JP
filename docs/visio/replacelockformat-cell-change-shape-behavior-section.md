---
title: '[ReplaceLockFormat] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。 マスター シェイプの ReplaceLockFormat セルは、(1) は、TRUE に設定されている場合、マスター シェイプの書式設定の値はマスターによって置換される図形のすべてに対応する値を上書きします。
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806202"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="98c3d-104">[ReplaceLockFormat] セル ([図形の動作の変更] セクション)</span><span class="sxs-lookup"><span data-stu-id="98c3d-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="98c3d-105">マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="98c3d-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="98c3d-106">マスター シェイプの**ReplaceLockFormat**セルは、(1) は、TRUE に設定されている場合、マスター シェイプの書式設定の値はマスターによって置換される図形のすべてに対応する値を上書きします。</span><span class="sxs-lookup"><span data-stu-id="98c3d-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="98c3d-107">**値**</span><span class="sxs-lookup"><span data-stu-id="98c3d-107">**Value**</span></span>|<span data-ttu-id="98c3d-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="98c3d-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98c3d-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="98c3d-109">TRUE</span></span>  <br/> |<span data-ttu-id="98c3d-110">マスター シェイプの**ReplaceLockFormat**セルを TRUE に設定すると、マスター シェイプの書式設定の値は交換するため、マスター シェイプのすべての対応する値を上書きします。</span><span class="sxs-lookup"><span data-stu-id="98c3d-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="98c3d-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="98c3d-111">FALSE</span></span>  <br/> |<span data-ttu-id="98c3d-112">マスター シェイプの**ReplaceLockFormat**セルが FALSE に設定されている場合、置換後の図形には、置換操作後に古い図形のローカル書式設定値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="98c3d-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98c3d-113">備考</span><span class="sxs-lookup"><span data-stu-id="98c3d-113">Remarks</span></span>

<span data-ttu-id="98c3d-114">**ReplaceLockFormat**セルでは、マスター シェイプが図形の置換操作の実行中に次のセクションのセルのローカルの書式設定値を上書きするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="98c3d-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="98c3d-115">**塗りつぶしの書式**セクション</span><span class="sxs-lookup"><span data-stu-id="98c3d-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="98c3d-116">**行の書式**セクション</span><span class="sxs-lookup"><span data-stu-id="98c3d-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="98c3d-117">[**クイック スタイル**]</span><span class="sxs-lookup"><span data-stu-id="98c3d-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="98c3d-118">**テーマのプロパティ**] セクション</span><span class="sxs-lookup"><span data-stu-id="98c3d-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="98c3d-119">**グラデーションのプロパティ**] セクション</span><span class="sxs-lookup"><span data-stu-id="98c3d-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="98c3d-120">**傾斜面のプロパティ**] セクション</span><span class="sxs-lookup"><span data-stu-id="98c3d-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="98c3d-121">**その他のエフェクトのプロパティ**] セクション</span><span class="sxs-lookup"><span data-stu-id="98c3d-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="98c3d-122">**グラデーション終了位置の行**セクション</span><span class="sxs-lookup"><span data-stu-id="98c3d-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="98c3d-123">**グラデーション終了位置の設定**] セクション</span><span class="sxs-lookup"><span data-stu-id="98c3d-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="98c3d-124">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReplaceLockFormat** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="98c3d-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="98c3d-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="98c3d-125">Cell name:</span></span>  <br/> | <span data-ttu-id="98c3d-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="98c3d-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="98c3d-127">プログラムから、インデックスによって [ **ReplaceLockFormat** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="98c3d-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="98c3d-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="98c3d-128">Section index:</span></span>  <br/> |<span data-ttu-id="98c3d-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="98c3d-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="98c3d-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="98c3d-130">Row index:</span></span>  <br/> |<span data-ttu-id="98c3d-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="98c3d-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="98c3d-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="98c3d-132">Cell index:</span></span>  <br/> |<span data-ttu-id="98c3d-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="98c3d-133">**visReplaceLockFormat**</span></span> <br/> |
   

