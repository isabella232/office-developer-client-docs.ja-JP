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
ms.openlocfilehash: 981f4f417e48f70d0693e30683c4351d0e53a758
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805777"
---
# <a name="lockmovex-cell-protection-section"></a><span data-ttu-id="bda29-103">[LockMoveX] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="bda29-103">LockMoveX Cell (Protection Section)</span></span>

<span data-ttu-id="bda29-104">図形の水平位置をロックします。ロックすると、図形は水平方向に移動できなくなります。</span><span class="sxs-lookup"><span data-stu-id="bda29-104">Locks the horizontal position of the shape so it cannot be moved horizontally.</span></span>
  
|<span data-ttu-id="bda29-105">**値**</span><span class="sxs-lookup"><span data-stu-id="bda29-105">**Value**</span></span>|<span data-ttu-id="bda29-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="bda29-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bda29-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bda29-107">TRUE</span></span>  <br/> | <span data-ttu-id="bda29-108">水平位置をロックします。</span><span class="sxs-lookup"><span data-stu-id="bda29-108">Horizontal position is locked.</span></span>  <br/> |
| <span data-ttu-id="bda29-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bda29-109">FALSE</span></span>  <br/> | <span data-ttu-id="bda29-110">水平位置をロックしません。</span><span class="sxs-lookup"><span data-stu-id="bda29-110">Horizontal position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bda29-111">備考</span><span class="sxs-lookup"><span data-stu-id="bda29-111">Remarks</span></span>

<span data-ttu-id="bda29-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockMoveX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bda29-112">To get a reference to the LockMoveX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bda29-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="bda29-113">Cell name:</span></span>  <br/> | <span data-ttu-id="bda29-114">[Lockmovex]</span><span class="sxs-lookup"><span data-stu-id="bda29-114">LockMoveX</span></span>  <br/> |
   
<span data-ttu-id="bda29-115">プログラムから、インデックスによって [LockMoveX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bda29-115">To get a reference to the LockMoveX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bda29-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bda29-116">Section index:</span></span>  <br/> |<span data-ttu-id="bda29-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bda29-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bda29-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bda29-118">Row index:</span></span>  <br/> |<span data-ttu-id="bda29-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="bda29-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="bda29-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bda29-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bda29-121">**visLockMoveX**</span><span class="sxs-lookup"><span data-stu-id="bda29-121">**visLockMoveX**</span></span> <br/> |
   

