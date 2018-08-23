---
title: '[LockFormat] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: 図形の書式設定をロックして、変更できないようにします。
ms.openlocfilehash: c3e4d5be848e91554406e709ce6872ae49b5f38d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805753"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="66e89-103">[LockFormat] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="66e89-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="66e89-104">図形の書式設定をロックして、変更できないようにします。</span><span class="sxs-lookup"><span data-stu-id="66e89-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="66e89-105">**値**</span><span class="sxs-lookup"><span data-stu-id="66e89-105">**Value**</span></span>|<span data-ttu-id="66e89-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="66e89-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="66e89-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="66e89-107">TRUE</span></span>  <br/> | <span data-ttu-id="66e89-108">書式を変更できません。</span><span class="sxs-lookup"><span data-stu-id="66e89-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="66e89-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="66e89-109">FALSE</span></span>  <br/> | <span data-ttu-id="66e89-110">書式を変更できます。</span><span class="sxs-lookup"><span data-stu-id="66e89-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66e89-111">備考</span><span class="sxs-lookup"><span data-stu-id="66e89-111">Remarks</span></span>

<span data-ttu-id="66e89-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockFormat] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="66e89-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66e89-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="66e89-113">Cell name:</span></span>  <br/> | <span data-ttu-id="66e89-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="66e89-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="66e89-115">プログラムから、インデックスによって [LockFormat] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="66e89-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66e89-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="66e89-116">Section index:</span></span>  <br/> |<span data-ttu-id="66e89-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="66e89-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="66e89-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="66e89-118">Row index:</span></span>  <br/> |<span data-ttu-id="66e89-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="66e89-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="66e89-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="66e89-120">Cell index:</span></span>  <br/> |<span data-ttu-id="66e89-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="66e89-121">**visLockFormat**</span></span> <br/> |
   

