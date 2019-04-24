---
title: '[LockCalcWH] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: 図形の選択範囲をロックして、頂点を編集した場合や、行の種類を [Geometry] セクションで変更した場合に再計算できないようにします。
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359634"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="473e1-103">[LockCalcWH] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="473e1-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="473e1-104">図形の選択範囲をロックして、頂点を編集した場合や、行の種類を [Geometry] セクションで変更した場合に再計算できないようにします。</span><span class="sxs-lookup"><span data-stu-id="473e1-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="473e1-105">**値**</span><span class="sxs-lookup"><span data-stu-id="473e1-105">**Value**</span></span>|<span data-ttu-id="473e1-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="473e1-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="473e1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="473e1-107">TRUE</span></span>  <br/> | <span data-ttu-id="473e1-108">幅と高さを再計算できません。</span><span class="sxs-lookup"><span data-stu-id="473e1-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="473e1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="473e1-109">FALSE</span></span>  <br/> | <span data-ttu-id="473e1-110">幅と高さを再計算できます。</span><span class="sxs-lookup"><span data-stu-id="473e1-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="473e1-111">解説</span><span class="sxs-lookup"><span data-stu-id="473e1-111">Remarks</span></span>

<span data-ttu-id="473e1-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockCalcWH] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="473e1-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="473e1-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="473e1-113">Cell name:</span></span>  <br/> | <span data-ttu-id="473e1-114">[lockcalcwh]</span><span class="sxs-lookup"><span data-stu-id="473e1-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="473e1-115">プログラムから、インデックスによって [LockCalcWH] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="473e1-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="473e1-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="473e1-116">Section index:</span></span>  <br/> |<span data-ttu-id="473e1-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="473e1-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="473e1-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="473e1-118">Row index:</span></span>  <br/> |<span data-ttu-id="473e1-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="473e1-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="473e1-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="473e1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="473e1-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="473e1-121">**visLockCalcWH**</span></span> <br/> |
   

