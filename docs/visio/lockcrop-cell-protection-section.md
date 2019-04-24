---
title: '[LockCrop] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: 別のプログラムのオブジェクトをロックして、[トリミング ツール] を使用したトリミングができないようにします。
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359627"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="44981-103">[LockCrop] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="44981-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="44981-104">別のプログラムのオブジェクトをロックして、[**トリミング ツール**] を使用したトリミングができないようにします。</span><span class="sxs-lookup"><span data-stu-id="44981-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="44981-105">**値**</span><span class="sxs-lookup"><span data-stu-id="44981-105">**Value**</span></span>|<span data-ttu-id="44981-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="44981-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="44981-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="44981-107">TRUE</span></span>  <br/> | <span data-ttu-id="44981-108">図形はトリミングできません。</span><span class="sxs-lookup"><span data-stu-id="44981-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="44981-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="44981-109">FALSE</span></span>  <br/> | <span data-ttu-id="44981-110">図形はトリミングできます。</span><span class="sxs-lookup"><span data-stu-id="44981-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44981-111">解説</span><span class="sxs-lookup"><span data-stu-id="44981-111">Remarks</span></span>

<span data-ttu-id="44981-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockCrop] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="44981-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="44981-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="44981-113">Cell name:</span></span>  <br/> | <span data-ttu-id="44981-114">[lockcrop]</span><span class="sxs-lookup"><span data-stu-id="44981-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="44981-115">プログラムから、インデックスによって [LockCrop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="44981-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="44981-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="44981-116">Section index:</span></span>  <br/> |<span data-ttu-id="44981-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="44981-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="44981-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="44981-118">Row index:</span></span>  <br/> |<span data-ttu-id="44981-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="44981-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="44981-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="44981-120">Cell index:</span></span>  <br/> |<span data-ttu-id="44981-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="44981-121">**visLockCrop**</span></span> <br/> |
   

