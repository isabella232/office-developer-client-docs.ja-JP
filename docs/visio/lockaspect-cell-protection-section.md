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
ms.openlocfilehash: fb5736add65f548f06697077bc539ec7fac5feb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805747"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="37693-103">[LockAspect] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="37693-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="37693-104">図形の縦横比をロックします。ロックすると、図形のサイズを変更するときに縦横比が維持されます。上下、左右のいずれか一方向だけサイズを変更することができなくなります。</span><span class="sxs-lookup"><span data-stu-id="37693-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="37693-105">**値**</span><span class="sxs-lookup"><span data-stu-id="37693-105">**Value**</span></span>|<span data-ttu-id="37693-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="37693-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="37693-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="37693-107">TRUE</span></span>  <br/> | <span data-ttu-id="37693-108">縦横比をロックします。</span><span class="sxs-lookup"><span data-stu-id="37693-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="37693-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="37693-109">FALSE</span></span>  <br/> | <span data-ttu-id="37693-110">縦横比をロックしません。</span><span class="sxs-lookup"><span data-stu-id="37693-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37693-111">備考</span><span class="sxs-lookup"><span data-stu-id="37693-111">Remarks</span></span>

<span data-ttu-id="37693-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockAspect] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="37693-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37693-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="37693-113">Cell name:</span></span>  <br/> | <span data-ttu-id="37693-114">LockAspect</span><span class="sxs-lookup"><span data-stu-id="37693-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="37693-115">プログラムから、インデックスによって [LockAspect] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="37693-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37693-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="37693-116">Section index:</span></span>  <br/> |<span data-ttu-id="37693-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37693-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="37693-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="37693-118">Row index:</span></span>  <br/> |<span data-ttu-id="37693-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="37693-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="37693-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="37693-120">Cell index:</span></span>  <br/> |<span data-ttu-id="37693-121">**visLockAspect**</span><span class="sxs-lookup"><span data-stu-id="37693-121">**visLockAspect**</span></span> <br/> |
   

