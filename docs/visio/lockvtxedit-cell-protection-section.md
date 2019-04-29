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
ms.openlocfilehash: 1703769fe54171a14f7052f0f6686e1eb5ec92fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417667"
---
# <a name="lockvtxedit-cell-protection-section"></a><span data-ttu-id="b1639-103">[LockVtxEdit] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="b1639-103">LockVtxEdit Cell (Protection Section)</span></span>

<span data-ttu-id="b1639-104">図形の頂点をロックします。ロックすると、頂点を編集できなくなります。</span><span class="sxs-lookup"><span data-stu-id="b1639-104">Locks the vertices of a shape so that they cannot be edited.</span></span>
  
|<span data-ttu-id="b1639-105">**値**</span><span class="sxs-lookup"><span data-stu-id="b1639-105">**Value**</span></span>|<span data-ttu-id="b1639-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="b1639-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1639-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b1639-107">TRUE</span></span>  <br/> |<span data-ttu-id="b1639-108">頂点を編集できません。</span><span class="sxs-lookup"><span data-stu-id="b1639-108">Vertices cannot be edited.</span></span>  <br/> |
|<span data-ttu-id="b1639-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b1639-109">FALSE</span></span>  <br/> |<span data-ttu-id="b1639-110">頂点を編集できます。</span><span class="sxs-lookup"><span data-stu-id="b1639-110">Vertices can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1639-111">注釈</span><span class="sxs-lookup"><span data-stu-id="b1639-111">Remarks</span></span>

<span data-ttu-id="b1639-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockVtxEdit] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b1639-112">To get a reference to the LockVtxEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1639-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="b1639-113">Cell name:</span></span>  <br/> |<span data-ttu-id="b1639-114">[lockvtxedit]</span><span class="sxs-lookup"><span data-stu-id="b1639-114">LockVtxEdit</span></span>  <br/> |
   
<span data-ttu-id="b1639-115">プログラムから、インデックスによって [LockVtxEdit] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1639-115">To get a reference to the LockVtxEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1639-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1639-116">Section index:</span></span>  <br/> |<span data-ttu-id="b1639-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b1639-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b1639-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1639-118">Row index:</span></span>  <br/> |<span data-ttu-id="b1639-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="b1639-119">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="b1639-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1639-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b1639-121">**visLockVtxEdit**</span><span class="sxs-lookup"><span data-stu-id="b1639-121">**visLockVtxEdit**</span></span> <br/> |
   

