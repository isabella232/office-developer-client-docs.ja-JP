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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423042"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="a6116-103">[LockCalcWH] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="a6116-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="a6116-104">図形の選択範囲をロックして、頂点を編集した場合や、行の種類を [Geometry] セクションで変更した場合に再計算できないようにします。</span><span class="sxs-lookup"><span data-stu-id="a6116-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="a6116-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a6116-105">**Value**</span></span>|<span data-ttu-id="a6116-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a6116-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a6116-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a6116-107">TRUE</span></span>  <br/> | <span data-ttu-id="a6116-108">幅と高さを再計算できません。</span><span class="sxs-lookup"><span data-stu-id="a6116-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="a6116-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a6116-109">FALSE</span></span>  <br/> | <span data-ttu-id="a6116-110">幅と高さを再計算できます。</span><span class="sxs-lookup"><span data-stu-id="a6116-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6116-111">注釈</span><span class="sxs-lookup"><span data-stu-id="a6116-111">Remarks</span></span>

<span data-ttu-id="a6116-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockCalcWH] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6116-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6116-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="a6116-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a6116-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="a6116-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="a6116-115">プログラムから、インデックスによって [LockCalcWH] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6116-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6116-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a6116-116">Section index:</span></span>  <br/> |<span data-ttu-id="a6116-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a6116-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a6116-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a6116-118">Row index:</span></span>  <br/> |<span data-ttu-id="a6116-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="a6116-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="a6116-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a6116-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a6116-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="a6116-121">**visLockCalcWH**</span></span> <br/> |
   

