---
title: '[DynFeedback] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: コネクタをドラッグしたときにユーザーに対して表示されるフィードバックの種類を変更します。マウス ボタンを離した後に表示されるコネクタ図形は、この設定の影響を受けません。またこの設定は、経路指定が可能なコネクタには適用されません。
ms.openlocfilehash: 858d98c8ee55eb49f58bbe98491ddc8752e75504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805298"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="9c658-105">[DynFeedback] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="9c658-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="9c658-p102">コネクタをドラッグしたときにユーザーに対して表示されるフィードバックの種類を変更します。マウス ボタンを離した後に表示されるコネクタ図形は、この設定の影響を受けません。またこの設定は、経路指定が可能なコネクタには適用されません。</span><span class="sxs-lookup"><span data-stu-id="9c658-p102">Changes the type of visual feedback provided to users when they drag a connector. When the mouse button is released, the resulting connector shape is not affected by this setting. This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="9c658-109">**値**</span><span class="sxs-lookup"><span data-stu-id="9c658-109">**Value**</span></span>|<span data-ttu-id="9c658-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="9c658-110">**Description**</span></span>|<span data-ttu-id="9c658-111">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="9c658-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9c658-112">0</span><span class="sxs-lookup"><span data-stu-id="9c658-112">0</span></span>  <br/> | <span data-ttu-id="9c658-113">直線を維持します (脚なし)。</span><span class="sxs-lookup"><span data-stu-id="9c658-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="9c658-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="9c658-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="9c658-115">1</span><span class="sxs-lookup"><span data-stu-id="9c658-115">1</span></span>  <br/> | <span data-ttu-id="9c658-116">ドラッグすると脚を 3 本表示します。</span><span class="sxs-lookup"><span data-stu-id="9c658-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="9c658-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="9c658-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="9c658-118">2</span><span class="sxs-lookup"><span data-stu-id="9c658-118">2</span></span>  <br/> | <span data-ttu-id="9c658-119">ドラッグすると脚を 5 本表示します。</span><span class="sxs-lookup"><span data-stu-id="9c658-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="9c658-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="9c658-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c658-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="9c658-121">Remarks</span></span>

<span data-ttu-id="9c658-122">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DynFeedback] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="9c658-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c658-123">セル名 :</span><span class="sxs-lookup"><span data-stu-id="9c658-123">Cell name:</span></span>  <br/> | <span data-ttu-id="9c658-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="9c658-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="9c658-125">プログラムから、インデックスによって [DynFeedback] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9c658-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c658-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c658-126">Section index:</span></span>  <br/> |<span data-ttu-id="9c658-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9c658-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9c658-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c658-128">Row index:</span></span>  <br/> |<span data-ttu-id="9c658-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="9c658-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="9c658-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c658-130">Cell index:</span></span>  <br/> |<span data-ttu-id="9c658-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="9c658-131">**visDynFeedback**</span></span> <br/> |
   

