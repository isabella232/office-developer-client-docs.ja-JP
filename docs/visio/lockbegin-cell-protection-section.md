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
ms.openlocfilehash: c9b9a0e9b69de9b76d78ca7cebfb69116bd2fb72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805736"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="d5aee-103">[LockBegin] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="d5aee-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="d5aee-104">1-D 図形の始点 ([BeginX]、[BeginY]) を特定の位置にロックします。</span><span class="sxs-lookup"><span data-stu-id="d5aee-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="d5aee-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d5aee-105">**Value**</span></span>|<span data-ttu-id="d5aee-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5aee-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d5aee-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d5aee-107">TRUE</span></span>  <br/> | <span data-ttu-id="d5aee-108">始点をロックします。</span><span class="sxs-lookup"><span data-stu-id="d5aee-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="d5aee-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d5aee-109">FALSE</span></span>  <br/> | <span data-ttu-id="d5aee-110">始点をロックしません。</span><span class="sxs-lookup"><span data-stu-id="d5aee-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5aee-111">備考</span><span class="sxs-lookup"><span data-stu-id="d5aee-111">Remarks</span></span>

<span data-ttu-id="d5aee-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockBegin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d5aee-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d5aee-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="d5aee-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d5aee-114">[Lockbegin]</span><span class="sxs-lookup"><span data-stu-id="d5aee-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="d5aee-115">プログラムから、インデックスによって [LockBegin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5aee-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d5aee-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d5aee-116">Section index:</span></span>  <br/> |<span data-ttu-id="d5aee-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d5aee-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d5aee-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d5aee-118">Row index:</span></span>  <br/> |<span data-ttu-id="d5aee-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d5aee-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d5aee-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d5aee-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d5aee-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="d5aee-121">**visLockBegin**</span></span> <br/> |
   

