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
description: トリミング ツールでトリミングされている別のプログラムからオブジェクトをロックします。
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805748"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="4eec7-103">[LockCrop] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="4eec7-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="4eec7-104">**トリミング**ツールでトリミングされている別のプログラムからオブジェクトをロックします。</span><span class="sxs-lookup"><span data-stu-id="4eec7-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="4eec7-105">**値**</span><span class="sxs-lookup"><span data-stu-id="4eec7-105">**Value**</span></span>|<span data-ttu-id="4eec7-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="4eec7-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4eec7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4eec7-107">TRUE</span></span>  <br/> | <span data-ttu-id="4eec7-108">図形はトリミングできません。</span><span class="sxs-lookup"><span data-stu-id="4eec7-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="4eec7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4eec7-109">FALSE</span></span>  <br/> | <span data-ttu-id="4eec7-110">図形はトリミングできます。</span><span class="sxs-lookup"><span data-stu-id="4eec7-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4eec7-111">備考</span><span class="sxs-lookup"><span data-stu-id="4eec7-111">Remarks</span></span>

<span data-ttu-id="4eec7-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [lockcrop] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4eec7-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4eec7-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="4eec7-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4eec7-114">[Lockcrop]</span><span class="sxs-lookup"><span data-stu-id="4eec7-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="4eec7-115">プログラムから、インデックスによって [lockcrop] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4eec7-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4eec7-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4eec7-116">Section index:</span></span>  <br/> |<span data-ttu-id="4eec7-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4eec7-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4eec7-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4eec7-118">Row index:</span></span>  <br/> |<span data-ttu-id="4eec7-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="4eec7-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="4eec7-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4eec7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4eec7-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="4eec7-121">**visLockCrop**</span></span> <br/> |
   

