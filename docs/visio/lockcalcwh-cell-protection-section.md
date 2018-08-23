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
ms.openlocfilehash: f7f9c99eb4978e9b32968d3076b0341efe42faa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805742"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="d7452-103">[LockCalcWH] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="d7452-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="d7452-104">図形の選択範囲をロックして、頂点を編集した場合や、行の種類を [Geometry] セクションで変更した場合に再計算できないようにします。</span><span class="sxs-lookup"><span data-stu-id="d7452-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="d7452-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d7452-105">**Value**</span></span>|<span data-ttu-id="d7452-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d7452-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d7452-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d7452-107">TRUE</span></span>  <br/> | <span data-ttu-id="d7452-108">幅と高さを再計算できません。</span><span class="sxs-lookup"><span data-stu-id="d7452-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="d7452-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d7452-109">FALSE</span></span>  <br/> | <span data-ttu-id="d7452-110">幅と高さを再計算できます。</span><span class="sxs-lookup"><span data-stu-id="d7452-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7452-111">備考</span><span class="sxs-lookup"><span data-stu-id="d7452-111">Remarks</span></span>

<span data-ttu-id="d7452-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockCalcWH] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d7452-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7452-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="d7452-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d7452-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="d7452-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="d7452-115">プログラムから、インデックスによって [LockCalcWH] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7452-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7452-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d7452-116">Section index:</span></span>  <br/> |<span data-ttu-id="d7452-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d7452-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d7452-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d7452-118">Row index:</span></span>  <br/> |<span data-ttu-id="d7452-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d7452-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d7452-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d7452-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d7452-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="d7452-121">**visLockCalcWH**</span></span> <br/> |
   

