---
title: '[LockVtxEdit] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: 図形の頂点をロックします。ロックすると、頂点を編集できなくなります。
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805793"
---
# <a name="lockvtxedit-cell-protection-section"></a><span data-ttu-id="e317f-103">[LockVtxEdit] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="e317f-103">LockVtxEdit Cell (Protection Section)</span></span>

<span data-ttu-id="e317f-104">図形の頂点をロックします。ロックすると、頂点を編集できなくなります。</span><span class="sxs-lookup"><span data-stu-id="e317f-104">Locks the vertices of a shape so that they cannot be edited.</span></span>
  
|<span data-ttu-id="e317f-105">**値**</span><span class="sxs-lookup"><span data-stu-id="e317f-105">**Value**</span></span>|<span data-ttu-id="e317f-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="e317f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e317f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e317f-107">TRUE</span></span>  <br/> |<span data-ttu-id="e317f-108">頂点を編集できません。</span><span class="sxs-lookup"><span data-stu-id="e317f-108">Vertices cannot be edited.</span></span>  <br/> |
|<span data-ttu-id="e317f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e317f-109">FALSE</span></span>  <br/> |<span data-ttu-id="e317f-110">頂点を編集できます。</span><span class="sxs-lookup"><span data-stu-id="e317f-110">Vertices can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e317f-111">注釈</span><span class="sxs-lookup"><span data-stu-id="e317f-111">Remarks</span></span>

<span data-ttu-id="e317f-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockVtxEdit] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="e317f-112">To get a reference to the LockVtxEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e317f-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="e317f-113">Cell name:</span></span>  <br/> |<span data-ttu-id="e317f-114">LockVtxEdit</span><span class="sxs-lookup"><span data-stu-id="e317f-114">LockVtxEdit</span></span>  <br/> |
   
<span data-ttu-id="e317f-115">プログラムから、インデックスによって [LockVtxEdit] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e317f-115">To get a reference to the LockVtxEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e317f-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e317f-116">Section index:</span></span>  <br/> |<span data-ttu-id="e317f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e317f-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e317f-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e317f-118">Row index:</span></span>  <br/> |<span data-ttu-id="e317f-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e317f-119">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="e317f-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e317f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e317f-121">**visLockVtxEdit**</span><span class="sxs-lookup"><span data-stu-id="e317f-121">**visLockVtxEdit**</span></span> <br/> |
   

