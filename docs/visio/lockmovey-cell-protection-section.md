---
title: '[LockMoveY] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: 図形の垂直位置をロックします。ロックすると、図形は垂直方向に移動できなくなります。
ms.openlocfilehash: 6666d47555f8175b4950f95e1fb15abb8b11bfd5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434047"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="fc3ba-103">[LockMoveY] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="fc3ba-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="fc3ba-104">図形の垂直位置をロックします。ロックすると、図形は垂直方向に移動できなくなります。</span><span class="sxs-lookup"><span data-stu-id="fc3ba-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="fc3ba-105">**値**</span><span class="sxs-lookup"><span data-stu-id="fc3ba-105">**Value**</span></span>|<span data-ttu-id="fc3ba-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="fc3ba-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fc3ba-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fc3ba-107">TRUE</span></span>  <br/> | <span data-ttu-id="fc3ba-108">垂直位置をロックします。</span><span class="sxs-lookup"><span data-stu-id="fc3ba-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="fc3ba-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fc3ba-109">FALSE</span></span>  <br/> | <span data-ttu-id="fc3ba-110">垂直位置をロックしません。</span><span class="sxs-lookup"><span data-stu-id="fc3ba-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc3ba-111">注釈</span><span class="sxs-lookup"><span data-stu-id="fc3ba-111">Remarks</span></span>

<span data-ttu-id="fc3ba-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockMoveY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc3ba-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc3ba-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="fc3ba-113">Cell name:</span></span>  <br/> | <span data-ttu-id="fc3ba-114">[lockmovey]</span><span class="sxs-lookup"><span data-stu-id="fc3ba-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="fc3ba-115">プログラムから、インデックスによって [LockMoveY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fc3ba-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc3ba-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fc3ba-116">Section index:</span></span>  <br/> |<span data-ttu-id="fc3ba-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fc3ba-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fc3ba-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fc3ba-118">Row index:</span></span>  <br/> |<span data-ttu-id="fc3ba-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="fc3ba-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="fc3ba-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fc3ba-120">Cell index:</span></span>  <br/> |<span data-ttu-id="fc3ba-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="fc3ba-121">**visLockMoveY**</span></span> <br/> |
   

