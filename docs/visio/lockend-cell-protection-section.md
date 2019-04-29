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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425583"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="f49f9-103">[LockEnd] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="f49f9-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="f49f9-104">1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。</span><span class="sxs-lookup"><span data-stu-id="f49f9-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="f49f9-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f49f9-105">**Value**</span></span>|<span data-ttu-id="f49f9-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f49f9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f49f9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f49f9-107">TRUE</span></span>  <br/> | <span data-ttu-id="f49f9-108">終点をロックします。</span><span class="sxs-lookup"><span data-stu-id="f49f9-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="f49f9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f49f9-109">FALSE</span></span>  <br/> | <span data-ttu-id="f49f9-110">終点をロックしません。</span><span class="sxs-lookup"><span data-stu-id="f49f9-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f49f9-111">注釈</span><span class="sxs-lookup"><span data-stu-id="f49f9-111">Remarks</span></span>

<span data-ttu-id="f49f9-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockEnd] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f49f9-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f49f9-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="f49f9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f49f9-114">[lockend]</span><span class="sxs-lookup"><span data-stu-id="f49f9-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="f49f9-115">プログラムから、インデックスによって [LockEnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f49f9-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f49f9-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f49f9-116">Section index:</span></span>  <br/> |<span data-ttu-id="f49f9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f49f9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f49f9-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f49f9-118">Row index:</span></span>  <br/> |<span data-ttu-id="f49f9-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f49f9-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="f49f9-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f49f9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f49f9-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="f49f9-121">**visLockEnd**</span></span> <br/> |
   

