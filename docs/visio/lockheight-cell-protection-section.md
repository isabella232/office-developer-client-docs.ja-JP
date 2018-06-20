---
title: '[LockHeight] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: 図形の高さをロックします。ロックすると、図形のサイズを変更しても高さは変更されません。
ms.openlocfilehash: f6afe6037ff3d0810cc532bbc18bb749ee589bb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805760"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="4f552-103">[LockHeight] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="4f552-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="4f552-104">図形の高さをロックします。ロックすると、図形のサイズを変更しても高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="4f552-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="4f552-105">**値**</span><span class="sxs-lookup"><span data-stu-id="4f552-105">**Value**</span></span>|<span data-ttu-id="4f552-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="4f552-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4f552-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4f552-107">TRUE</span></span>  <br/> | <span data-ttu-id="4f552-108">高さをロックします。</span><span class="sxs-lookup"><span data-stu-id="4f552-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="4f552-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4f552-109">FALSE</span></span>  <br/> | <span data-ttu-id="4f552-110">高さをロックしません。</span><span class="sxs-lookup"><span data-stu-id="4f552-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f552-111">備考</span><span class="sxs-lookup"><span data-stu-id="4f552-111">Remarks</span></span>

<span data-ttu-id="4f552-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockHeight] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4f552-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f552-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="4f552-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4f552-114">LockHeight</span><span class="sxs-lookup"><span data-stu-id="4f552-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="4f552-115">プログラムから、インデックスによって [LockHeight] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4f552-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f552-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4f552-116">Section index:</span></span>  <br/> |<span data-ttu-id="4f552-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4f552-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4f552-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4f552-118">Row index:</span></span>  <br/> |<span data-ttu-id="4f552-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="4f552-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="4f552-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4f552-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4f552-121">**visLockHeight**</span><span class="sxs-lookup"><span data-stu-id="4f552-121">**visLockHeight**</span></span> <br/> |
   

