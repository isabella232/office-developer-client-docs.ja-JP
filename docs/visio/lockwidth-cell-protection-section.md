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
ms.openlocfilehash: abdcc0d5285e98e5856524925a41c4f72ee7f6ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805785"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="2a68b-103">[LockWidth] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="2a68b-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="2a68b-104">図形の幅をロックします。ロックすると、図形のサイズを変更しても幅は変更されません。</span><span class="sxs-lookup"><span data-stu-id="2a68b-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="2a68b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="2a68b-105">**Value**</span></span>|<span data-ttu-id="2a68b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="2a68b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2a68b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2a68b-107">TRUE</span></span>  <br/> | <span data-ttu-id="2a68b-108">幅をロックします。</span><span class="sxs-lookup"><span data-stu-id="2a68b-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="2a68b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2a68b-109">FALSE</span></span>  <br/> | <span data-ttu-id="2a68b-110">幅をロックしません。</span><span class="sxs-lookup"><span data-stu-id="2a68b-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a68b-111">備考</span><span class="sxs-lookup"><span data-stu-id="2a68b-111">Remarks</span></span>

<span data-ttu-id="2a68b-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [lockwidth] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="2a68b-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a68b-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="2a68b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2a68b-114">[Lockwidth]</span><span class="sxs-lookup"><span data-stu-id="2a68b-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="2a68b-115">プログラムから、インデックスによって [lockwidth] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="2a68b-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a68b-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2a68b-116">Section index:</span></span>  <br/> |<span data-ttu-id="2a68b-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2a68b-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2a68b-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2a68b-118">Row index:</span></span>  <br/> |<span data-ttu-id="2a68b-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2a68b-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2a68b-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2a68b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2a68b-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="2a68b-121">**visLockWidth**</span></span> <br/> |
   

