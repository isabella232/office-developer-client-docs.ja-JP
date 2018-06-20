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
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806261"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="13d0c-103">[ResizeMode] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="13d0c-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="13d0c-104">図形に対して現在設定されているサイズ変更の動作の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="13d0c-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="13d0c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="13d0c-105">**Value**</span></span>|<span data-ttu-id="13d0c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="13d0c-106">**Description**</span></span>|<span data-ttu-id="13d0c-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="13d0c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13d0c-108">0</span><span class="sxs-lookup"><span data-stu-id="13d0c-108">0</span></span>  <br/> |<span data-ttu-id="13d0c-109">グループの設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="13d0c-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="13d0c-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="13d0c-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="13d0c-111">1</span><span class="sxs-lookup"><span data-stu-id="13d0c-111">1</span></span>  <br/> |<span data-ttu-id="13d0c-112">位置のみを変更します。</span><span class="sxs-lookup"><span data-stu-id="13d0c-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="13d0c-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="13d0c-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="13d0c-114">2</span><span class="sxs-lookup"><span data-stu-id="13d0c-114">2</span></span>  <br/> |<span data-ttu-id="13d0c-115">グループに合わせてサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="13d0c-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="13d0c-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="13d0c-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13d0c-117">備考</span><span class="sxs-lookup"><span data-stu-id="13d0c-117">Remarks</span></span>

<span data-ttu-id="13d0c-118">[**動作**] タブ、[**動作**] ダイアログ ボックスでこの値を設定することもできます ([[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="13d0c-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="13d0c-119">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ResizeMode] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="13d0c-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13d0c-120">セル名:</span><span class="sxs-lookup"><span data-stu-id="13d0c-120">Cell name:</span></span>  <br/> |<span data-ttu-id="13d0c-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="13d0c-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="13d0c-122">プログラムから、インデックスによって [ResizeMode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="13d0c-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13d0c-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="13d0c-123">Section index:</span></span>  <br/> |<span data-ttu-id="13d0c-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="13d0c-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="13d0c-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="13d0c-125">Row index:</span></span>  <br/> |<span data-ttu-id="13d0c-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="13d0c-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="13d0c-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="13d0c-127">Cell index:</span></span>  <br/> |<span data-ttu-id="13d0c-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="13d0c-128">**visXFormResizeMode**</span></span> <br/> |
   

