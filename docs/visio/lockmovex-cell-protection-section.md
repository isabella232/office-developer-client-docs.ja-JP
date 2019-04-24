---
title: '[LockMoveX] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: 図形の水平位置をロックします。ロックすると、図形は水平方向に移動できなくなります。
ms.openlocfilehash: af0cee32370a540cd8d7aaf960cc0cbc27cc8f97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348266"
---
# <a name="lockmovex-cell-protection-section"></a><span data-ttu-id="a0029-103">[LockMoveX] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="a0029-103">LockMoveX Cell (Protection Section)</span></span>

<span data-ttu-id="a0029-104">図形の水平位置をロックします。ロックすると、図形は水平方向に移動できなくなります。</span><span class="sxs-lookup"><span data-stu-id="a0029-104">Locks the horizontal position of the shape so it cannot be moved horizontally.</span></span>
  
|<span data-ttu-id="a0029-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a0029-105">**Value**</span></span>|<span data-ttu-id="a0029-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a0029-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a0029-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a0029-107">TRUE</span></span>  <br/> | <span data-ttu-id="a0029-108">水平位置をロックします。</span><span class="sxs-lookup"><span data-stu-id="a0029-108">Horizontal position is locked.</span></span>  <br/> |
| <span data-ttu-id="a0029-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a0029-109">FALSE</span></span>  <br/> | <span data-ttu-id="a0029-110">水平位置をロックしません。</span><span class="sxs-lookup"><span data-stu-id="a0029-110">Horizontal position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0029-111">解説</span><span class="sxs-lookup"><span data-stu-id="a0029-111">Remarks</span></span>

<span data-ttu-id="a0029-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockMoveX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0029-112">To get a reference to the LockMoveX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a0029-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="a0029-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a0029-114">[lockmovex]</span><span class="sxs-lookup"><span data-stu-id="a0029-114">LockMoveX</span></span>  <br/> |
   
<span data-ttu-id="a0029-115">プログラムから、インデックスによって [LockMoveX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0029-115">To get a reference to the LockMoveX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a0029-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0029-116">Section index:</span></span>  <br/> |<span data-ttu-id="a0029-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0029-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a0029-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0029-118">Row index:</span></span>  <br/> |<span data-ttu-id="a0029-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="a0029-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="a0029-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0029-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a0029-121">**visLockMoveX**</span><span class="sxs-lookup"><span data-stu-id="a0029-121">**visLockMoveX**</span></span> <br/> |
   

