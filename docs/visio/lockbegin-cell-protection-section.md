---
title: '[LockBegin] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: 1-D 図形の始点 ([BeginX]、[BeginY]) を特定の位置にロックします。
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359648"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="be9e1-103">[LockBegin] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="be9e1-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="be9e1-104">1-D 図形の始点 ([BeginX]、[BeginY]) を特定の位置にロックします。</span><span class="sxs-lookup"><span data-stu-id="be9e1-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="be9e1-105">**値**</span><span class="sxs-lookup"><span data-stu-id="be9e1-105">**Value**</span></span>|<span data-ttu-id="be9e1-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="be9e1-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="be9e1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="be9e1-107">TRUE</span></span>  <br/> | <span data-ttu-id="be9e1-108">始点をロックします。</span><span class="sxs-lookup"><span data-stu-id="be9e1-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="be9e1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="be9e1-109">FALSE</span></span>  <br/> | <span data-ttu-id="be9e1-110">始点をロックしません。</span><span class="sxs-lookup"><span data-stu-id="be9e1-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be9e1-111">解説</span><span class="sxs-lookup"><span data-stu-id="be9e1-111">Remarks</span></span>

<span data-ttu-id="be9e1-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockBegin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="be9e1-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be9e1-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="be9e1-113">Cell name:</span></span>  <br/> | <span data-ttu-id="be9e1-114">[lockbegin]</span><span class="sxs-lookup"><span data-stu-id="be9e1-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="be9e1-115">プログラムから、インデックスによって [LockBegin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="be9e1-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be9e1-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="be9e1-116">Section index:</span></span>  <br/> |<span data-ttu-id="be9e1-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="be9e1-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="be9e1-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="be9e1-118">Row index:</span></span>  <br/> |<span data-ttu-id="be9e1-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="be9e1-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="be9e1-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="be9e1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="be9e1-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="be9e1-121">**visLockBegin**</span></span> <br/> |
   

