---
title: '[DynamicsOff] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: 図面ページ上にある他の図形やコネクタに合わせて、配置可能な図形を移動したり、コネクタを迂回させるかどうかを指定します。
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437477"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="13b52-103">[DynamicsOff] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="13b52-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="13b52-104">図面ページ上にある他の図形やコネクタに合わせて、配置可能な図形を移動したり、コネクタを迂回させるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="13b52-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="13b52-105">**値**</span><span class="sxs-lookup"><span data-stu-id="13b52-105">**Value**</span></span>|<span data-ttu-id="13b52-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="13b52-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="13b52-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="13b52-107">TRUE</span></span>  <br/> | <span data-ttu-id="13b52-108">動的な移動や迂回を無効にします。</span><span class="sxs-lookup"><span data-stu-id="13b52-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="13b52-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="13b52-109">FALSE</span></span>  <br/> | <span data-ttu-id="13b52-110">動的な移動や迂回を有効にします。</span><span class="sxs-lookup"><span data-stu-id="13b52-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13b52-111">注釈</span><span class="sxs-lookup"><span data-stu-id="13b52-111">Remarks</span></span>

<span data-ttu-id="13b52-p101">動的な移動や迂回を無効にすると、ソリューションのパフォーマンスが向上します。たとえば、ソリューションで図面に配置可能な図形を追加するとき、図形を追加するたびにコネクタの経路変更や、図形の再配置が実行されないようにするには、動的な移動や迂回を無効にします。ソリューションで図形をすべて追加した後に、動的な移動や迂回を再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="13b52-p101">You can disable dynamics to increase your solution's performance. For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics. After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="13b52-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DynamicsOff] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="13b52-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13b52-116">セル名 :</span><span class="sxs-lookup"><span data-stu-id="13b52-116">Cell name:</span></span>  <br/> | <span data-ttu-id="13b52-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="13b52-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="13b52-118">プログラムから、インデックスによって [DynamicsOff] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="13b52-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13b52-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="13b52-119">Section index:</span></span>  <br/> |<span data-ttu-id="13b52-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="13b52-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="13b52-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="13b52-121">Row index:</span></span>  <br/> |<span data-ttu-id="13b52-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="13b52-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="13b52-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="13b52-123">Cell index:</span></span>  <br/> |<span data-ttu-id="13b52-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="13b52-124">**visPLODynamicsOff**</span></span> <br/> |
   

