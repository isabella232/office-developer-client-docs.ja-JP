---
title: '[ResizeMode] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: 図形に対して現在設定されているサイズ変更の動作の方法を示します。
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326881"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="10d75-103">[ResizeMode] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="10d75-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="10d75-104">図形に対して現在設定されているサイズ変更の動作の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="10d75-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="10d75-105">**値**</span><span class="sxs-lookup"><span data-stu-id="10d75-105">**Value**</span></span>|<span data-ttu-id="10d75-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="10d75-106">**Description**</span></span>|<span data-ttu-id="10d75-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="10d75-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="10d75-108">.0</span><span class="sxs-lookup"><span data-stu-id="10d75-108">0</span></span>  <br/> |<span data-ttu-id="10d75-109">グループの設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="10d75-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="10d75-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="10d75-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="10d75-111">1-d</span><span class="sxs-lookup"><span data-stu-id="10d75-111">1</span></span>  <br/> |<span data-ttu-id="10d75-112">位置のみを変更します。</span><span class="sxs-lookup"><span data-stu-id="10d75-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="10d75-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="10d75-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="10d75-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="10d75-114">2</span></span>  <br/> |<span data-ttu-id="10d75-115">グループに合わせてサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="10d75-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="10d75-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="10d75-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10d75-117">解説</span><span class="sxs-lookup"><span data-stu-id="10d75-117">Remarks</span></span>

<span data-ttu-id="10d75-118">この値は、[**基本動作**] ダイアログボックス ([[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで、[**基本動作**] をクリック) の [**動作**] タブで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="10d75-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="10d75-119">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ResizeMode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="10d75-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10d75-120">セル名:</span><span class="sxs-lookup"><span data-stu-id="10d75-120">Cell name:</span></span>  <br/> |<span data-ttu-id="10d75-121">[resizemode]</span><span class="sxs-lookup"><span data-stu-id="10d75-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="10d75-122">プログラムから、インデックスによって [ResizeMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="10d75-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10d75-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="10d75-123">Section index:</span></span>  <br/> |<span data-ttu-id="10d75-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="10d75-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="10d75-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="10d75-125">Row index:</span></span>  <br/> |<span data-ttu-id="10d75-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="10d75-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="10d75-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="10d75-127">Cell index:</span></span>  <br/> |<span data-ttu-id="10d75-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="10d75-128">**visXFormResizeMode**</span></span> <br/> |
   

