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
description: 2 次元図形をロックして、回転ハンドル、[左へ 90 度回転] コマンド、[右へ 90 度回転] コマンドによる回転操作ができないようにします。
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404674"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="f4d98-103">[LockRotate] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="f4d98-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="f4d98-104">2 次元図形をロックして、回転ハンドル、[**左へ 90 度回転**] コマンド、[**右へ 90 度回転**] コマンドによる回転操作ができないようにします。</span><span class="sxs-lookup"><span data-stu-id="f4d98-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="f4d98-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f4d98-105">**Value**</span></span>|<span data-ttu-id="f4d98-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f4d98-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f4d98-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f4d98-107">TRUE</span></span>  <br/> | <span data-ttu-id="f4d98-108">図形を回転できません。</span><span class="sxs-lookup"><span data-stu-id="f4d98-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="f4d98-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f4d98-109">FALSE</span></span>  <br/> | <span data-ttu-id="f4d98-110">図形を回転できます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="f4d98-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4d98-111">注釈</span><span class="sxs-lookup"><span data-stu-id="f4d98-111">Remarks</span></span>

<span data-ttu-id="f4d98-p101">[LockRotate] セルを設定しても、1-D 図形は端点をドラッグして回転できます。1-D 図形の回転をロックするには、[LockWidth] セルをゼロ以外の値 (TRUE) に設定します。</span><span class="sxs-lookup"><span data-stu-id="f4d98-p101">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged. To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="f4d98-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockRotate] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4d98-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4d98-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="f4d98-115">Cell name:</span></span>  <br/> | <span data-ttu-id="f4d98-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="f4d98-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="f4d98-117">プログラムから、インデックスによって [LockRotate] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4d98-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4d98-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4d98-118">Section index:</span></span>  <br/> |<span data-ttu-id="f4d98-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f4d98-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f4d98-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4d98-120">Row index:</span></span>  <br/> |<span data-ttu-id="f4d98-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f4d98-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="f4d98-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4d98-122">Cell index:</span></span>  <br/> |<span data-ttu-id="f4d98-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="f4d98-123">**visLockRotate**</span></span> <br/> |
   

