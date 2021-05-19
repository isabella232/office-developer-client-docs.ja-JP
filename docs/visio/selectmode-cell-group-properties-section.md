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
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435363"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="6d755-103">[SelectMode] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="6d755-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="6d755-104">グループ図形とそのメンバーを選択する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d755-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="6d755-105">**値**</span><span class="sxs-lookup"><span data-stu-id="6d755-105">**Value**</span></span>|<span data-ttu-id="6d755-106">**選択モード**</span><span class="sxs-lookup"><span data-stu-id="6d755-106">**Selection mode**</span></span>|<span data-ttu-id="6d755-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="6d755-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6d755-108">0</span><span class="sxs-lookup"><span data-stu-id="6d755-108">0</span></span>  <br/> |<span data-ttu-id="6d755-109">グループ図形だけを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d755-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="6d755-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="6d755-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="6d755-111">1</span><span class="sxs-lookup"><span data-stu-id="6d755-111">1</span></span>  <br/> |<span data-ttu-id="6d755-112">グループ図形を最初に選択します。</span><span class="sxs-lookup"><span data-stu-id="6d755-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="6d755-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="6d755-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="6d755-114">2</span><span class="sxs-lookup"><span data-stu-id="6d755-114">2</span></span>  <br/> |<span data-ttu-id="6d755-115">グループのメンバーを最初に選択します。</span><span class="sxs-lookup"><span data-stu-id="6d755-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="6d755-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="6d755-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d755-117">注釈</span><span class="sxs-lookup"><span data-stu-id="6d755-117">Remarks</span></span>

<span data-ttu-id="6d755-118">この値は、[動作] ダイアログボックスで設定することもできます (グループ図形が選択されている場合は、[開発]タブの [図形のデザイン] グループで、[動作]をクリックし、[グループの動作] の下の [選択] リストでモードをクリック **します**)。 [](run-in-developer-mode-display-the-developer-tab.md) </span><span class="sxs-lookup"><span data-stu-id="6d755-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="6d755-119">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SelectMode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6d755-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d755-120">セル名 :</span><span class="sxs-lookup"><span data-stu-id="6d755-120">Cell name:</span></span>  <br/> |<span data-ttu-id="6d755-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="6d755-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="6d755-122">プログラムから、インデックスによって [SelectMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d755-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d755-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6d755-123">Section index:</span></span>  <br/> |<span data-ttu-id="6d755-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6d755-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6d755-125">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="6d755-125">Row index:</span></span>  <br/> |<span data-ttu-id="6d755-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="6d755-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="6d755-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6d755-127">Cell index:</span></span>  <br/> |<span data-ttu-id="6d755-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="6d755-128">**visGroupSelectMode**</span></span> <br/> |
   

