---
title: '[LockAspect] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: 図形の縦横比をロックします。ロックすると、図形のサイズを変更するときに縦横比が維持されます。上下、左右のいずれか一方向だけサイズを変更することができなくなります。
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359641"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="965af-103">[LockAspect] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="965af-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="965af-104">図形の縦横比をロックします。ロックすると、図形のサイズを変更するときに縦横比が維持されます。上下、左右のいずれか一方向だけサイズを変更することができなくなります。</span><span class="sxs-lookup"><span data-stu-id="965af-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="965af-105">**値**</span><span class="sxs-lookup"><span data-stu-id="965af-105">**Value**</span></span>|<span data-ttu-id="965af-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="965af-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="965af-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="965af-107">TRUE</span></span>  <br/> | <span data-ttu-id="965af-108">縦横比をロックします。</span><span class="sxs-lookup"><span data-stu-id="965af-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="965af-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="965af-109">FALSE</span></span>  <br/> | <span data-ttu-id="965af-110">縦横比をロックしません。</span><span class="sxs-lookup"><span data-stu-id="965af-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="965af-111">解説</span><span class="sxs-lookup"><span data-stu-id="965af-111">Remarks</span></span>

<span data-ttu-id="965af-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockAspect] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="965af-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="965af-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="965af-113">Cell name:</span></span>  <br/> | <span data-ttu-id="965af-114">[lockaspect]</span><span class="sxs-lookup"><span data-stu-id="965af-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="965af-115">プログラムから、インデックスによって [LockAspect] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="965af-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="965af-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="965af-116">Section index:</span></span>  <br/> |<span data-ttu-id="965af-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="965af-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="965af-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="965af-118">Row index:</span></span>  <br/> |<span data-ttu-id="965af-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="965af-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="965af-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="965af-120">Cell index:</span></span>  <br/> |<span data-ttu-id="965af-121">**visLockAspect**</span><span class="sxs-lookup"><span data-stu-id="965af-121">**visLockAspect**</span></span> <br/> |
   

