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
ms.openlocfilehash: 24f6f477860ea3634cfdcfd92199f2de65e543db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805759"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="3e607-103">[LockMoveY] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="3e607-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="3e607-104">図形の垂直位置をロックします。ロックすると、図形は垂直方向に移動できなくなります。</span><span class="sxs-lookup"><span data-stu-id="3e607-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="3e607-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3e607-105">**Value**</span></span>|<span data-ttu-id="3e607-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="3e607-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3e607-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3e607-107">TRUE</span></span>  <br/> | <span data-ttu-id="3e607-108">垂直位置をロックします。</span><span class="sxs-lookup"><span data-stu-id="3e607-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="3e607-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3e607-109">FALSE</span></span>  <br/> | <span data-ttu-id="3e607-110">垂直位置をロックしません。</span><span class="sxs-lookup"><span data-stu-id="3e607-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e607-111">備考</span><span class="sxs-lookup"><span data-stu-id="3e607-111">Remarks</span></span>

<span data-ttu-id="3e607-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [lockmovey] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="3e607-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3e607-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="3e607-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3e607-114">[Lockmovey]</span><span class="sxs-lookup"><span data-stu-id="3e607-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="3e607-115">プログラムから、インデックスによって [lockmovey] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e607-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3e607-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3e607-116">Section index:</span></span>  <br/> |<span data-ttu-id="3e607-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3e607-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3e607-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3e607-118">Row index:</span></span>  <br/> |<span data-ttu-id="3e607-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="3e607-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="3e607-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3e607-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3e607-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="3e607-121">**visLockMoveY**</span></span> <br/> |
   

