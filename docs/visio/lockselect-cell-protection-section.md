---
title: '[LockSelect] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: 図形の選択操作ができないようにします。
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805780"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="73d0c-103">[LockSelect] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="73d0c-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="73d0c-104">図形の選択操作ができないようにします。</span><span class="sxs-lookup"><span data-stu-id="73d0c-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="73d0c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="73d0c-105">**Value**</span></span>|<span data-ttu-id="73d0c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="73d0c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="73d0c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="73d0c-107">TRUE</span></span>  <br/> | <span data-ttu-id="73d0c-108">図形を選択できません。</span><span class="sxs-lookup"><span data-stu-id="73d0c-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="73d0c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="73d0c-109">FALSE</span></span>  <br/> | <span data-ttu-id="73d0c-110">図形を選択できます。</span><span class="sxs-lookup"><span data-stu-id="73d0c-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73d0c-111">備考</span><span class="sxs-lookup"><span data-stu-id="73d0c-111">Remarks</span></span>

<span data-ttu-id="73d0c-112">[LockSelect] を有効にするには、[**図面の保護**] ダイアログ ボックスの [**図形**] チェック ボックスをオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="73d0c-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="73d0c-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockSelect] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="73d0c-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="73d0c-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="73d0c-114">Cell name:</span></span>  <br/> | <span data-ttu-id="73d0c-115">Lockselect] を有効</span><span class="sxs-lookup"><span data-stu-id="73d0c-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="73d0c-116">プログラムから、インデックスによって [LockSelect] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="73d0c-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="73d0c-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="73d0c-117">Section index:</span></span>  <br/> |<span data-ttu-id="73d0c-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="73d0c-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="73d0c-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="73d0c-119">Row index:</span></span>  <br/> |<span data-ttu-id="73d0c-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="73d0c-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="73d0c-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="73d0c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="73d0c-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="73d0c-122">**visLockSelect**</span></span> <br/> |
   

