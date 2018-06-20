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
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805601"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="d6bbe-103">[IsDropSource] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="d6bbe-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="d6bbe-104">図形をドロップしてグループに追加できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d6bbe-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="d6bbe-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d6bbe-105">**Value**</span></span>|<span data-ttu-id="d6bbe-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d6bbe-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6bbe-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d6bbe-107">TRUE</span></span>  <br/> |<span data-ttu-id="d6bbe-108">図形をドロップしてグループに追加できます。</span><span class="sxs-lookup"><span data-stu-id="d6bbe-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="d6bbe-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d6bbe-109">FALSE</span></span>  <br/> |<span data-ttu-id="d6bbe-110">図形をドロップしてグループに追加できません。</span><span class="sxs-lookup"><span data-stu-id="d6bbe-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6bbe-111">注釈</span><span class="sxs-lookup"><span data-stu-id="d6bbe-111">Remarks</span></span>

<span data-ttu-id="d6bbe-112">図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、[**動作**] をクリックし、[**ドロップ時にグループに図形を追加**する] チェック ボックスを選択してこの値を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d6bbe-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="d6bbe-113">図形に対してこの動作を有効にするには、ほかにドラッグされた図形を受け入れるようにグループを有効にする必要がありますもします。</span><span class="sxs-lookup"><span data-stu-id="d6bbe-113">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it.</span></span> <span data-ttu-id="d6bbe-114">これを行うには、グループを選択し、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、[**動作**] をクリックし、[**ドロップした図形を受け入れる**] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d6bbe-114">To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box.</span></span> <span data-ttu-id="d6bbe-115">この値は、グループのプロパティ] セクションで [IsDropTarget] セルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="d6bbe-115">This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="d6bbe-116">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[IsDropSource] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d6bbe-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6bbe-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="d6bbe-117">Cell name:</span></span>  <br/> |<span data-ttu-id="d6bbe-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="d6bbe-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="d6bbe-119">プログラムから、インデックスによって [IsDropSource] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d6bbe-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6bbe-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d6bbe-120">Section index:</span></span>  <br/> |<span data-ttu-id="d6bbe-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d6bbe-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d6bbe-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d6bbe-122">Row index:</span></span>  <br/> |<span data-ttu-id="d6bbe-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="d6bbe-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="d6bbe-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d6bbe-124">Cell index:</span></span>  <br/> |<span data-ttu-id="d6bbe-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="d6bbe-125">**visDropSource**</span></span> <br/> |
   

