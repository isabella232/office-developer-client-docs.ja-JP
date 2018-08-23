---
title: '[LockGroup] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: グループをロックして、グループを解除できないようにします。
ms.openlocfilehash: 4d09d514a3fff8ada40c67eb9cd9537539a1039a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805773"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="15030-103">[LockGroup] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="15030-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="15030-104">グループをロックして、グループを解除できないようにします。</span><span class="sxs-lookup"><span data-stu-id="15030-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="15030-105">**値**</span><span class="sxs-lookup"><span data-stu-id="15030-105">**Value**</span></span>|<span data-ttu-id="15030-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="15030-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15030-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="15030-107">TRUE</span></span>  <br/> |<span data-ttu-id="15030-108">グループを解除できません。</span><span class="sxs-lookup"><span data-stu-id="15030-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="15030-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="15030-109">FALSE</span></span>  <br/> |<span data-ttu-id="15030-110">グループを解除できます。</span><span class="sxs-lookup"><span data-stu-id="15030-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15030-111">注釈</span><span class="sxs-lookup"><span data-stu-id="15030-111">Remarks</span></span>

<span data-ttu-id="15030-112">[LockGroupCell] 値を TRUE に設定すると、グループのメンバーである図形が削除されるのを防ぐこともできます。</span><span class="sxs-lookup"><span data-stu-id="15030-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="15030-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockGroup] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="15030-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15030-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="15030-114">Cell name:</span></span>  <br/> |<span data-ttu-id="15030-115">[Lockgroup]</span><span class="sxs-lookup"><span data-stu-id="15030-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="15030-116">プログラムから、インデックスによって [LockGroup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="15030-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15030-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="15030-117">Section index:</span></span>  <br/> |<span data-ttu-id="15030-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="15030-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="15030-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="15030-119">Row index:</span></span>  <br/> |<span data-ttu-id="15030-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="15030-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="15030-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="15030-121">Cell index:</span></span>  <br/> |<span data-ttu-id="15030-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="15030-122">**visLockGroup**</span></span> <br/> |
   

