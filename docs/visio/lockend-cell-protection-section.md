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
ms.openlocfilehash: d29f07e5b4b77ed2fb8b104769a2fdca55abcc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805754"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="99da3-103">[LockEnd] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="99da3-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="99da3-104">1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。</span><span class="sxs-lookup"><span data-stu-id="99da3-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="99da3-105">**値**</span><span class="sxs-lookup"><span data-stu-id="99da3-105">**Value**</span></span>|<span data-ttu-id="99da3-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="99da3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="99da3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="99da3-107">TRUE</span></span>  <br/> | <span data-ttu-id="99da3-108">終点をロックします。</span><span class="sxs-lookup"><span data-stu-id="99da3-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="99da3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="99da3-109">FALSE</span></span>  <br/> | <span data-ttu-id="99da3-110">終点をロックしません。</span><span class="sxs-lookup"><span data-stu-id="99da3-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99da3-111">備考</span><span class="sxs-lookup"><span data-stu-id="99da3-111">Remarks</span></span>

<span data-ttu-id="99da3-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [lockend] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="99da3-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99da3-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="99da3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="99da3-114">[Lockend]</span><span class="sxs-lookup"><span data-stu-id="99da3-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="99da3-115">プログラムから、インデックスによって [lockend] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="99da3-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99da3-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="99da3-116">Section index:</span></span>  <br/> |<span data-ttu-id="99da3-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="99da3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="99da3-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="99da3-118">Row index:</span></span>  <br/> |<span data-ttu-id="99da3-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="99da3-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="99da3-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="99da3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="99da3-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="99da3-121">**visLockEnd**</span></span> <br/> |
   

