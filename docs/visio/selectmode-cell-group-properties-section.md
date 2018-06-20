---
title: '[SelectMode] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: グループ図形とそのメンバーを選択する方法を指定します。
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806363"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="ca691-103">[SelectMode] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="ca691-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="ca691-104">グループ図形とそのメンバーを選択する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca691-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="ca691-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ca691-105">**Value**</span></span>|<span data-ttu-id="ca691-106">**選択モード**</span><span class="sxs-lookup"><span data-stu-id="ca691-106">**Selection mode**</span></span>|<span data-ttu-id="ca691-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="ca691-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca691-108">0</span><span class="sxs-lookup"><span data-stu-id="ca691-108">0</span></span>  <br/> |<span data-ttu-id="ca691-109">グループ図形だけを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca691-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="ca691-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="ca691-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="ca691-111">1</span><span class="sxs-lookup"><span data-stu-id="ca691-111">1</span></span>  <br/> |<span data-ttu-id="ca691-112">グループ図形を最初に選択します。</span><span class="sxs-lookup"><span data-stu-id="ca691-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="ca691-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="ca691-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="ca691-114">2</span><span class="sxs-lookup"><span data-stu-id="ca691-114">2</span></span>  <br/> |<span data-ttu-id="ca691-115">グループのメンバーを最初に選択します。</span><span class="sxs-lookup"><span data-stu-id="ca691-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="ca691-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="ca691-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca691-117">備考</span><span class="sxs-lookup"><span data-stu-id="ca691-117">Remarks</span></span>

<span data-ttu-id="ca691-118">**動作**] ダイアログ ボックスでこの値を設定することもできます (グループ図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、**グループの下**の選択**ボックスの一覧でモードをクリックし、動作**)。</span><span class="sxs-lookup"><span data-stu-id="ca691-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="ca691-119">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[SelectMode] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ca691-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca691-120">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ca691-120">Cell name:</span></span>  <br/> |<span data-ttu-id="ca691-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="ca691-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="ca691-122">プログラムから、インデックスによって [SelectMode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ca691-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca691-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ca691-123">Section index:</span></span>  <br/> |<span data-ttu-id="ca691-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca691-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ca691-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ca691-125">Row index:</span></span>  <br/> |<span data-ttu-id="ca691-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="ca691-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="ca691-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ca691-127">Cell index:</span></span>  <br/> |<span data-ttu-id="ca691-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="ca691-128">**visGroupSelectMode**</span></span> <br/> |
   

