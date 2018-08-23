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
ms.openlocfilehash: 00229dcabf45d2a3435039ffe05fd7eb4de75808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805751"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="d2ead-103">[LockDelete] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="d2ead-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="d2ead-104">図形をロックして、削除できないようにします。</span><span class="sxs-lookup"><span data-stu-id="d2ead-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="d2ead-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d2ead-105">**Value**</span></span>|<span data-ttu-id="d2ead-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d2ead-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d2ead-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d2ead-107">TRUE</span></span>  <br/> | <span data-ttu-id="d2ead-108">図形は削除できません。</span><span class="sxs-lookup"><span data-stu-id="d2ead-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="d2ead-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d2ead-109">FALSE</span></span>  <br/> | <span data-ttu-id="d2ead-110">図形は削除できます。</span><span class="sxs-lookup"><span data-stu-id="d2ead-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2ead-111">備考</span><span class="sxs-lookup"><span data-stu-id="d2ead-111">Remarks</span></span>

<span data-ttu-id="d2ead-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockDelete] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d2ead-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2ead-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="d2ead-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d2ead-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="d2ead-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="d2ead-115">プログラムから、インデックスによって [LockDelete] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2ead-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2ead-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2ead-116">Section index:</span></span>  <br/> |<span data-ttu-id="d2ead-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d2ead-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d2ead-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2ead-118">Row index:</span></span>  <br/> |<span data-ttu-id="d2ead-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d2ead-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d2ead-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2ead-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d2ead-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="d2ead-121">**visLockDelete**</span></span> <br/> |
   

