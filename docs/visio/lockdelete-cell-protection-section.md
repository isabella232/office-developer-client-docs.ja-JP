---
title: '[LockDelete] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: 図形をロックして、削除できないようにします。
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359620"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="e741d-103">[LockDelete] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="e741d-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="e741d-104">図形をロックして、削除できないようにします。</span><span class="sxs-lookup"><span data-stu-id="e741d-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="e741d-105">**値**</span><span class="sxs-lookup"><span data-stu-id="e741d-105">**Value**</span></span>|<span data-ttu-id="e741d-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="e741d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e741d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e741d-107">TRUE</span></span>  <br/> | <span data-ttu-id="e741d-108">図形は削除できません。</span><span class="sxs-lookup"><span data-stu-id="e741d-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="e741d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e741d-109">FALSE</span></span>  <br/> | <span data-ttu-id="e741d-110">図形は削除できます。</span><span class="sxs-lookup"><span data-stu-id="e741d-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e741d-111">解説</span><span class="sxs-lookup"><span data-stu-id="e741d-111">Remarks</span></span>

<span data-ttu-id="e741d-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockDelete] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e741d-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e741d-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="e741d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e741d-114">[lockdelete]</span><span class="sxs-lookup"><span data-stu-id="e741d-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="e741d-115">プログラムから、インデックスによって [LockDelete] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e741d-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e741d-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e741d-116">Section index:</span></span>  <br/> |<span data-ttu-id="e741d-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e741d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e741d-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e741d-118">Row index:</span></span>  <br/> |<span data-ttu-id="e741d-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e741d-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="e741d-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e741d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e741d-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="e741d-121">**visLockDelete**</span></span> <br/> |
   

