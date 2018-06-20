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
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="d85de-103">[LockFormat] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="d85de-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="d85de-104">図形の書式設定をロックして、変更できないようにします。</span><span class="sxs-lookup"><span data-stu-id="d85de-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="d85de-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d85de-105">**Value**</span></span>|<span data-ttu-id="d85de-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d85de-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d85de-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d85de-107">TRUE</span></span>  <br/> | <span data-ttu-id="d85de-108">書式を変更できません。</span><span class="sxs-lookup"><span data-stu-id="d85de-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="d85de-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d85de-109">FALSE</span></span>  <br/> | <span data-ttu-id="d85de-110">書式を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d85de-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d85de-111">備考</span><span class="sxs-lookup"><span data-stu-id="d85de-111">Remarks</span></span>

<span data-ttu-id="d85de-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockFormat] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d85de-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d85de-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="d85de-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d85de-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="d85de-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="d85de-115">プログラムから、インデックスによって [LockFormat] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d85de-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d85de-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d85de-116">Section index:</span></span>  <br/> |<span data-ttu-id="d85de-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d85de-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d85de-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d85de-118">Row index:</span></span>  <br/> |<span data-ttu-id="d85de-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d85de-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d85de-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d85de-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d85de-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="d85de-121">**visLockFormat**</span></span> <br/> |
   

