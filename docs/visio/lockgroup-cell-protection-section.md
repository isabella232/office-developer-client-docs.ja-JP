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
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404310"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="9a77c-103">[LockGroup] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="9a77c-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="9a77c-104">グループをロックして、グループを解除できないようにします。</span><span class="sxs-lookup"><span data-stu-id="9a77c-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="9a77c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="9a77c-105">**Value**</span></span>|<span data-ttu-id="9a77c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="9a77c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a77c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9a77c-107">TRUE</span></span>  <br/> |<span data-ttu-id="9a77c-108">グループを解除できません。</span><span class="sxs-lookup"><span data-stu-id="9a77c-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="9a77c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9a77c-109">FALSE</span></span>  <br/> |<span data-ttu-id="9a77c-110">グループを解除できます。</span><span class="sxs-lookup"><span data-stu-id="9a77c-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a77c-111">注釈</span><span class="sxs-lookup"><span data-stu-id="9a77c-111">Remarks</span></span>

<span data-ttu-id="9a77c-112">[LockGroupCell] 値を TRUE に設定すると、グループのメンバーである図形が削除されるのを防ぐこともできます。</span><span class="sxs-lookup"><span data-stu-id="9a77c-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="9a77c-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockGroup] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9a77c-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a77c-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="9a77c-114">Cell name:</span></span>  <br/> |<span data-ttu-id="9a77c-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="9a77c-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="9a77c-116">プログラムから、インデックスによって [LockGroup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a77c-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a77c-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9a77c-117">Section index:</span></span>  <br/> |<span data-ttu-id="9a77c-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9a77c-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9a77c-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9a77c-119">Row index:</span></span>  <br/> |<span data-ttu-id="9a77c-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="9a77c-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="9a77c-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9a77c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="9a77c-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="9a77c-122">**visLockGroup**</span></span> <br/> |
   

