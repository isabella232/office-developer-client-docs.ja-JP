---
title: '[LockWidth] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: 図形の幅をロックします。ロックすると、図形のサイズを変更しても幅は変更されません。
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439808"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="d3e58-103">[LockWidth] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="d3e58-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="d3e58-104">図形の幅をロックします。ロックすると、図形のサイズを変更しても幅は変更されません。</span><span class="sxs-lookup"><span data-stu-id="d3e58-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="d3e58-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d3e58-105">**Value**</span></span>|<span data-ttu-id="d3e58-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d3e58-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d3e58-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d3e58-107">TRUE</span></span>  <br/> | <span data-ttu-id="d3e58-108">幅をロックします。</span><span class="sxs-lookup"><span data-stu-id="d3e58-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="d3e58-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d3e58-109">FALSE</span></span>  <br/> | <span data-ttu-id="d3e58-110">幅をロックしません。</span><span class="sxs-lookup"><span data-stu-id="d3e58-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3e58-111">注釈</span><span class="sxs-lookup"><span data-stu-id="d3e58-111">Remarks</span></span>

<span data-ttu-id="d3e58-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockWidth] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3e58-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3e58-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="d3e58-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d3e58-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="d3e58-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="d3e58-115">プログラムから、インデックスによって [LockWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3e58-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3e58-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d3e58-116">Section index:</span></span>  <br/> |<span data-ttu-id="d3e58-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d3e58-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d3e58-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d3e58-118">Row index:</span></span>  <br/> |<span data-ttu-id="d3e58-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d3e58-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d3e58-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d3e58-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d3e58-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="d3e58-121">**visLockWidth**</span></span> <br/> |
   

