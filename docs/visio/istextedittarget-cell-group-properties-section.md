---
title: '[IsTextEditTarget] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: グループに対するテキストの割り当て方を指定します。
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432647"
---
# <a name="istextedittarget-cell-group-properties-section"></a><span data-ttu-id="8f143-103">[IsTextEditTarget] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="8f143-103">IsTextEditTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="8f143-104">グループに対するテキストの割り当て方を指定します。</span><span class="sxs-lookup"><span data-stu-id="8f143-104">Determines text assignment for a group.</span></span>
  
|<span data-ttu-id="8f143-105">**値**</span><span class="sxs-lookup"><span data-stu-id="8f143-105">**Value**</span></span>|<span data-ttu-id="8f143-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="8f143-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8f143-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8f143-107">TRUE</span></span>  <br/> |<span data-ttu-id="8f143-108">テキストはグループ図形に追加されます。</span><span class="sxs-lookup"><span data-stu-id="8f143-108">Text is added to the group shape.</span></span>  <br/> |
|<span data-ttu-id="8f143-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8f143-109">FALSE</span></span>  <br/> |<span data-ttu-id="8f143-110">テキストは、グループ内で積み重ねられた図形の中で、最前面にある図形に追加されます。</span><span class="sxs-lookup"><span data-stu-id="8f143-110">Text is added to the shape in the group at the top of the stacking order.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f143-111">注釈</span><span class="sxs-lookup"><span data-stu-id="8f143-111">Remarks</span></span>

<span data-ttu-id="8f143-112">このセルの値は、グループを選択して、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブで [**基本動作**] をクリックし、[**グループのテキストを編集**] チェック ボックスをオンにして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="8f143-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Edit text of group** check box.</span></span> 
  
<span data-ttu-id="8f143-p101">Visio 2000 より前のバージョンで作成したグループの場合、既定値は FALSE です。Visio バージョン 2000 以降、既定値は TRUE になっています。</span><span class="sxs-lookup"><span data-stu-id="8f143-p101">Groups created in versions earlier than Visio 2000 have a default value of FALSE. Beginning with Visio version 2000, the default value is TRUE.</span></span> 
  
<span data-ttu-id="8f143-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IsTextEditTarget] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f143-115">To get a reference to the IsTextEditTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f143-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="8f143-116">Cell name:</span></span>  <br/> |<span data-ttu-id="8f143-117">IsTextEditTarget</span><span class="sxs-lookup"><span data-stu-id="8f143-117">IsTextEditTarget</span></span>  <br/> |
   
<span data-ttu-id="8f143-118">プログラムから、インデックスによって [IsTextEditTarget] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8f143-118">To get a reference to the IsTextEditTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f143-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8f143-119">Section index:</span></span>  <br/> |<span data-ttu-id="8f143-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8f143-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8f143-121">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="8f143-121">Row index:</span></span>  <br/> |<span data-ttu-id="8f143-122">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="8f143-122">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="8f143-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8f143-123">Cell index:</span></span>  <br/> |<span data-ttu-id="8f143-124">**visGroupIsTextEditTarget**</span><span class="sxs-lookup"><span data-stu-id="8f143-124">**visGroupIsTextEditTarget**</span></span> <br/> |
   

