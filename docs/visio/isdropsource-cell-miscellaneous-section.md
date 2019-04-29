---
title: '[IsDropSource] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: 図形をドロップしてグループに追加できるかどうかを指定します。
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421894"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="45325-103">[IsDropSource] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="45325-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="45325-104">図形をドロップしてグループに追加できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="45325-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="45325-105">**値**</span><span class="sxs-lookup"><span data-stu-id="45325-105">**Value**</span></span>|<span data-ttu-id="45325-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="45325-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="45325-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="45325-107">TRUE</span></span>  <br/> |<span data-ttu-id="45325-108">図形をドロップしてグループに追加できます。</span><span class="sxs-lookup"><span data-stu-id="45325-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="45325-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="45325-109">FALSE</span></span>  <br/> |<span data-ttu-id="45325-110">図形をドロップしてグループに追加できません。</span><span class="sxs-lookup"><span data-stu-id="45325-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45325-111">注釈</span><span class="sxs-lookup"><span data-stu-id="45325-111">Remarks</span></span>

<span data-ttu-id="45325-112">このセルの値は、図形を選択して、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブで [**基本動作**] をクリックし、[**ドロップ時にグループに図形を追加**] チェック ボックスをオンにして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="45325-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="45325-p101">図形に対してこの動作を有効にする場合、グループに対しても、そのグループにドラッグされた図形を受け入れるように設定する必要があります。このように設定するには、グループを選択して [[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブで [**基本動作**] をクリックし、[**ドロップした図形を受け入れる**] チェック ボックスをオンにします。この値は、[Group Properties] セクションの [IsDropTarget] セルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="45325-p101">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it. To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box. This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="45325-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IsDropSource] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="45325-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45325-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="45325-117">Cell name:</span></span>  <br/> |<span data-ttu-id="45325-118">[isdropsource]</span><span class="sxs-lookup"><span data-stu-id="45325-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="45325-119">プログラムから、インデックスによって [IsDropSource] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="45325-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45325-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="45325-120">Section index:</span></span>  <br/> |<span data-ttu-id="45325-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="45325-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="45325-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="45325-122">Row index:</span></span>  <br/> |<span data-ttu-id="45325-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="45325-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="45325-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="45325-124">Cell index:</span></span>  <br/> |<span data-ttu-id="45325-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="45325-125">**visDropSource**</span></span> <br/> |
   

