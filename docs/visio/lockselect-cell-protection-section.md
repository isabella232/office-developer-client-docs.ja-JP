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
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409756"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="663b5-103">[LockSelect] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="663b5-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="663b5-104">図形の選択操作ができないようにします。</span><span class="sxs-lookup"><span data-stu-id="663b5-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="663b5-105">**値**</span><span class="sxs-lookup"><span data-stu-id="663b5-105">**Value**</span></span>|<span data-ttu-id="663b5-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="663b5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="663b5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="663b5-107">TRUE</span></span>  <br/> | <span data-ttu-id="663b5-108">図形を選択できません。</span><span class="sxs-lookup"><span data-stu-id="663b5-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="663b5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="663b5-109">FALSE</span></span>  <br/> | <span data-ttu-id="663b5-110">図形を選択できます。</span><span class="sxs-lookup"><span data-stu-id="663b5-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="663b5-111">注釈</span><span class="sxs-lookup"><span data-stu-id="663b5-111">Remarks</span></span>

<span data-ttu-id="663b5-112">[LockSelect] を有効にするには、[**図面の保護**] ダイアログ ボックスの [**図形**] チェック ボックスをオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="663b5-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="663b5-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockSelect] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="663b5-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="663b5-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="663b5-114">Cell name:</span></span>  <br/> | <span data-ttu-id="663b5-115">[lockselect]</span><span class="sxs-lookup"><span data-stu-id="663b5-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="663b5-116">プログラムから、インデックスによって [LockSelect] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="663b5-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="663b5-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="663b5-117">Section index:</span></span>  <br/> |<span data-ttu-id="663b5-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="663b5-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="663b5-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="663b5-119">Row index:</span></span>  <br/> |<span data-ttu-id="663b5-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="663b5-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="663b5-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="663b5-121">Cell index:</span></span>  <br/> |<span data-ttu-id="663b5-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="663b5-122">**visLockSelect**</span></span> <br/> |
   

