---
title: '[IsDropTarget] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: グループにドロップされた図形を、そのグループが受け入れるかどうかを決定します。
ms.openlocfilehash: 50f545b3cbd4f7e1541a7f5e8ca32c34d0429c5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297229"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="2955b-103">[IsDropTarget] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="2955b-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="2955b-104">グループにドロップされた図形を、そのグループが受け入れるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2955b-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="2955b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="2955b-105">**Value**</span></span>|<span data-ttu-id="2955b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="2955b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2955b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2955b-107">TRUE</span></span>  <br/> |<span data-ttu-id="2955b-108">グループは、ドロップされた図形を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="2955b-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="2955b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2955b-109">FALSE</span></span>  <br/> |<span data-ttu-id="2955b-110">グループは、ドロップされた図形を受け入れません。</span><span class="sxs-lookup"><span data-stu-id="2955b-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2955b-111">解説</span><span class="sxs-lookup"><span data-stu-id="2955b-111">Remarks</span></span>

<span data-ttu-id="2955b-112">このセルの値は、グループを選択して、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**基本動作**] をクリックし、[**ドロップした図形を受け入れる**] チェック ボックスをオンにして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="2955b-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="2955b-p101">図形をグループ上にドロップしてそのグループに追加するには、図形に対してもこの動作を有効にする必要があります。有効にするには、図形を選択して [[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**基本動作**] をクリックし、[**ドロップ時にグループに図形を追加**] チェック ボックスをオンにします。この値は、[Miscellaneous] セクションの [IsDropSource] セルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="2955b-p101">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior. You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box. This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="2955b-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IsDropTarget] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2955b-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2955b-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="2955b-117">Cell name:</span></span>  <br/> |<span data-ttu-id="2955b-118">[isdroptarget]</span><span class="sxs-lookup"><span data-stu-id="2955b-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="2955b-119">プログラムから、インデックスによって [IsDropTarget] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2955b-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2955b-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2955b-120">Section index:</span></span>  <br/> |<span data-ttu-id="2955b-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2955b-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2955b-122">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="2955b-122">Row index:</span></span>  <br/> |<span data-ttu-id="2955b-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="2955b-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="2955b-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2955b-124">Cell index:</span></span>  <br/> |<span data-ttu-id="2955b-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="2955b-125">**visGroupIsDropTarget**</span></span> <br/> |
   

