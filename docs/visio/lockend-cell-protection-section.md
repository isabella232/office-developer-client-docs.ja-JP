---
title: '[LockEnd] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: 1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359599"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="e10ce-103">[LockEnd] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="e10ce-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="e10ce-104">1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。</span><span class="sxs-lookup"><span data-stu-id="e10ce-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="e10ce-105">**値**</span><span class="sxs-lookup"><span data-stu-id="e10ce-105">**Value**</span></span>|<span data-ttu-id="e10ce-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="e10ce-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e10ce-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e10ce-107">TRUE</span></span>  <br/> | <span data-ttu-id="e10ce-108">終点をロックします。</span><span class="sxs-lookup"><span data-stu-id="e10ce-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="e10ce-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e10ce-109">FALSE</span></span>  <br/> | <span data-ttu-id="e10ce-110">終点をロックしません。</span><span class="sxs-lookup"><span data-stu-id="e10ce-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e10ce-111">解説</span><span class="sxs-lookup"><span data-stu-id="e10ce-111">Remarks</span></span>

<span data-ttu-id="e10ce-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockEnd] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e10ce-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e10ce-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="e10ce-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e10ce-114">[lockend]</span><span class="sxs-lookup"><span data-stu-id="e10ce-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="e10ce-115">プログラムから、インデックスによって [LockEnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e10ce-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e10ce-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e10ce-116">Section index:</span></span>  <br/> |<span data-ttu-id="e10ce-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e10ce-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e10ce-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e10ce-118">Row index:</span></span>  <br/> |<span data-ttu-id="e10ce-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e10ce-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="e10ce-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e10ce-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e10ce-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="e10ce-121">**visLockEnd**</span></span> <br/> |
   

