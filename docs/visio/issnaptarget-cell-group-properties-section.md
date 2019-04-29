---
title: '[IsSnapTarget] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: グループにスナップするかグループ内の図形にスナップするかを指定します。
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421446"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="b94b0-103">[IsSnapTarget] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="b94b0-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="b94b0-104">グループにスナップするかグループ内の図形にスナップするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b94b0-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="b94b0-105">**値**</span><span class="sxs-lookup"><span data-stu-id="b94b0-105">**Value**</span></span>|<span data-ttu-id="b94b0-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="b94b0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b94b0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b94b0-107">TRUE</span></span>  <br/> |<span data-ttu-id="b94b0-108">グループ内の図形へのスナップを有効にします。</span><span class="sxs-lookup"><span data-stu-id="b94b0-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="b94b0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b94b0-109">FALSE</span></span>  <br/> |<span data-ttu-id="b94b0-110">グループにのみスナップします。</span><span class="sxs-lookup"><span data-stu-id="b94b0-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b94b0-111">注釈</span><span class="sxs-lookup"><span data-stu-id="b94b0-111">Remarks</span></span>

<span data-ttu-id="b94b0-112">このセルの値は、グループを選択して、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**基本動作**] をクリックし、[**メンバー図形にスナップ**] チェック ボックスをオンにして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b94b0-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="b94b0-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IsSnapTarget] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b94b0-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b94b0-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="b94b0-114">Cell name:</span></span>  <br/> |<span data-ttu-id="b94b0-115">[issnaptarget]</span><span class="sxs-lookup"><span data-stu-id="b94b0-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="b94b0-116">プログラムから、インデックスによって [IsSnapTarget] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b94b0-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b94b0-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b94b0-117">Section index:</span></span>  <br/> |<span data-ttu-id="b94b0-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b94b0-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b94b0-119">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="b94b0-119">Row index:</span></span>  <br/> |<span data-ttu-id="b94b0-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="b94b0-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="b94b0-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b94b0-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b94b0-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="b94b0-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

