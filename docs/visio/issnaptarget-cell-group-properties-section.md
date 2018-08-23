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
ms.openlocfilehash: 89536923617f80768d7c14658cb07c97595824ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805626"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="38657-103">[IsSnapTarget] セル ([グループのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="38657-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="38657-104">グループにスナップするかグループ内の図形にスナップするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="38657-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="38657-105">**値**</span><span class="sxs-lookup"><span data-stu-id="38657-105">**Value**</span></span>|<span data-ttu-id="38657-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="38657-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38657-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="38657-107">TRUE</span></span>  <br/> |<span data-ttu-id="38657-108">グループ内の図形へのスナップを有効にします。</span><span class="sxs-lookup"><span data-stu-id="38657-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="38657-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="38657-109">FALSE</span></span>  <br/> |<span data-ttu-id="38657-110">グループにのみスナップします。</span><span class="sxs-lookup"><span data-stu-id="38657-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38657-111">注釈</span><span class="sxs-lookup"><span data-stu-id="38657-111">Remarks</span></span>

<span data-ttu-id="38657-112">このセルの値は、グループを選択して、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**基本動作**] をクリックし、[**メンバー図形にスナップ**] チェック ボックスをオンにして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="38657-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="38657-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IsSnapTarget] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="38657-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38657-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="38657-114">Cell name:</span></span>  <br/> |<span data-ttu-id="38657-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="38657-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="38657-116">プログラムから、インデックスによって [IsSnapTarget] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="38657-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38657-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="38657-117">Section index:</span></span>  <br/> |<span data-ttu-id="38657-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="38657-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="38657-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="38657-119">Row index:</span></span>  <br/> |<span data-ttu-id="38657-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="38657-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="38657-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="38657-121">Cell index:</span></span>  <br/> |<span data-ttu-id="38657-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="38657-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

