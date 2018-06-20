---
title: '[LockRotate] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: 回転ハンドル、[左に 90 度回転で回転する 2 次元図形をロック 90 ° または 90 ° のコマンドを右 90 度回転します。
ms.openlocfilehash: 450fe4786594472d018b705df4678fe636390ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805769"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="3cc6a-103">[LockRotate] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="3cc6a-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="3cc6a-104">回転ハンドルや**左 90 度の回転**、[**右 90 度回転**] コマンドで回転する 2 次元図形をロックします。</span><span class="sxs-lookup"><span data-stu-id="3cc6a-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="3cc6a-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3cc6a-105">**Value**</span></span>|<span data-ttu-id="3cc6a-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="3cc6a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3cc6a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3cc6a-107">TRUE</span></span>  <br/> | <span data-ttu-id="3cc6a-108">図形を回転できません。</span><span class="sxs-lookup"><span data-stu-id="3cc6a-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="3cc6a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3cc6a-109">FALSE</span></span>  <br/> | <span data-ttu-id="3cc6a-110">図形を回転できます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="3cc6a-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cc6a-111">備考</span><span class="sxs-lookup"><span data-stu-id="3cc6a-111">Remarks</span></span>

<span data-ttu-id="3cc6a-p101">[LockRotate] セルを設定しても、1-D 図形は端点をドラッグして回転できます。1-D 図形の回転をロックするには、[LockWidth] セルをゼロ以外の値 (TRUE) に設定します。</span><span class="sxs-lookup"><span data-stu-id="3cc6a-p101">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged. To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="3cc6a-114">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockRotate] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="3cc6a-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3cc6a-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="3cc6a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="3cc6a-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="3cc6a-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="3cc6a-117">プログラムから、インデックスによって [LockRotate] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3cc6a-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3cc6a-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3cc6a-118">Section index:</span></span>  <br/> |<span data-ttu-id="3cc6a-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3cc6a-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3cc6a-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3cc6a-120">Row index:</span></span>  <br/> |<span data-ttu-id="3cc6a-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="3cc6a-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="3cc6a-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3cc6a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3cc6a-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="3cc6a-123">**visLockRotate**</span></span> <br/> |
   

