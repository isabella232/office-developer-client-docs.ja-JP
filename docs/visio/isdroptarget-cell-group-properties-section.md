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
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805611"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="a9cb3-103">[IsDropTarget] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="a9cb3-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="a9cb3-104">グループにドロップされた図形を、そのグループが受け入れるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9cb3-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="a9cb3-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a9cb3-105">**Value**</span></span>|<span data-ttu-id="a9cb3-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a9cb3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a9cb3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a9cb3-107">TRUE</span></span>  <br/> |<span data-ttu-id="a9cb3-108">グループは、ドロップされた図形を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="a9cb3-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="a9cb3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a9cb3-109">FALSE</span></span>  <br/> |<span data-ttu-id="a9cb3-110">グループは、ドロップされた図形を受け入れません。</span><span class="sxs-lookup"><span data-stu-id="a9cb3-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9cb3-111">注釈</span><span class="sxs-lookup"><span data-stu-id="a9cb3-111">Remarks</span></span>

<span data-ttu-id="a9cb3-112">[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブ**の動作**をクリックすると、グループを選択し、**ドロップした図形を受け入れる**] チェック ボックスをオンを選択してこの値を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a9cb3-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="a9cb3-113">グループにドロップしてグループに図形を追加するものような図形の動作を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9cb3-113">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior.</span></span> <span data-ttu-id="a9cb3-114">図形を選択し、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、[**動作**] をクリックして、[**ドロップ時にグループに図形を追加**する] チェック ボックスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9cb3-114">You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box.</span></span> <span data-ttu-id="a9cb3-115">この値は、[その他] セクションの IsDropSource セルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="a9cb3-115">This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="a9cb3-116">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[IsDropTarget] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a9cb3-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9cb3-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="a9cb3-117">Cell name:</span></span>  <br/> |<span data-ttu-id="a9cb3-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="a9cb3-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="a9cb3-119">プログラムから、インデックスによって [IsDropTarget] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a9cb3-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9cb3-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a9cb3-120">Section index:</span></span>  <br/> |<span data-ttu-id="a9cb3-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a9cb3-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a9cb3-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a9cb3-122">Row index:</span></span>  <br/> |<span data-ttu-id="a9cb3-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="a9cb3-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="a9cb3-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a9cb3-124">Cell index:</span></span>  <br/> |<span data-ttu-id="a9cb3-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="a9cb3-125">**visGroupIsDropTarget**</span></span> <br/> |
   

