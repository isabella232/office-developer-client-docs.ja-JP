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
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404800"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="9cf0b-105">[DynFeedback] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="9cf0b-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="9cf0b-p102">コネクタをドラッグしたときにユーザーに対して表示されるフィードバックの種類を変更します。マウス ボタンを離した後に表示されるコネクタ図形は、この設定の影響を受けません。またこの設定は、経路指定が可能なコネクタには適用されません。</span><span class="sxs-lookup"><span data-stu-id="9cf0b-p102">Changes the type of visual feedback provided to users when they drag a connector. When the mouse button is released, the resulting connector shape is not affected by this setting. This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="9cf0b-109">**値**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-109">**Value**</span></span>|<span data-ttu-id="9cf0b-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-110">**Description**</span></span>|<span data-ttu-id="9cf0b-111">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9cf0b-112">0</span><span class="sxs-lookup"><span data-stu-id="9cf0b-112">0</span></span>  <br/> | <span data-ttu-id="9cf0b-113">直線を維持します (脚なし)。</span><span class="sxs-lookup"><span data-stu-id="9cf0b-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="9cf0b-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="9cf0b-115">1</span><span class="sxs-lookup"><span data-stu-id="9cf0b-115">1</span></span>  <br/> | <span data-ttu-id="9cf0b-116">ドラッグすると脚を 3 本表示します。</span><span class="sxs-lookup"><span data-stu-id="9cf0b-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="9cf0b-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="9cf0b-118">2</span><span class="sxs-lookup"><span data-stu-id="9cf0b-118">2</span></span>  <br/> | <span data-ttu-id="9cf0b-119">ドラッグすると脚を 5 本表示します。</span><span class="sxs-lookup"><span data-stu-id="9cf0b-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="9cf0b-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cf0b-121">注釈</span><span class="sxs-lookup"><span data-stu-id="9cf0b-121">Remarks</span></span>

<span data-ttu-id="9cf0b-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DynFeedback] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9cf0b-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cf0b-123">セル名 :</span><span class="sxs-lookup"><span data-stu-id="9cf0b-123">Cell name:</span></span>  <br/> | <span data-ttu-id="9cf0b-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="9cf0b-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="9cf0b-125">プログラムから、インデックスによって [DynFeedback] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9cf0b-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cf0b-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9cf0b-126">Section index:</span></span>  <br/> |<span data-ttu-id="9cf0b-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9cf0b-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9cf0b-128">Row index:</span></span>  <br/> |<span data-ttu-id="9cf0b-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="9cf0b-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9cf0b-130">Cell index:</span></span>  <br/> |<span data-ttu-id="9cf0b-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-131">**visDynFeedback**</span></span> <br/> |
   

