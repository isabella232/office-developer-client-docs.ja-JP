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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411856"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="d83e9-103">[LockCrop] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="d83e9-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="d83e9-104">別のプログラムのオブジェクトをロックして、[**トリミング ツール**] を使用したトリミングができないようにします。</span><span class="sxs-lookup"><span data-stu-id="d83e9-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="d83e9-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d83e9-105">**Value**</span></span>|<span data-ttu-id="d83e9-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d83e9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d83e9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d83e9-107">TRUE</span></span>  <br/> | <span data-ttu-id="d83e9-108">図形はトリミングできません。</span><span class="sxs-lookup"><span data-stu-id="d83e9-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="d83e9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d83e9-109">FALSE</span></span>  <br/> | <span data-ttu-id="d83e9-110">図形はトリミングできます。</span><span class="sxs-lookup"><span data-stu-id="d83e9-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d83e9-111">注釈</span><span class="sxs-lookup"><span data-stu-id="d83e9-111">Remarks</span></span>

<span data-ttu-id="d83e9-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockCrop] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d83e9-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d83e9-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="d83e9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d83e9-114">LockCrop</span><span class="sxs-lookup"><span data-stu-id="d83e9-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="d83e9-115">プログラムから、インデックスによって [LockCrop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d83e9-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d83e9-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d83e9-116">Section index:</span></span>  <br/> |<span data-ttu-id="d83e9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d83e9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d83e9-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d83e9-118">Row index:</span></span>  <br/> |<span data-ttu-id="d83e9-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d83e9-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d83e9-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d83e9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d83e9-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="d83e9-121">**visLockCrop**</span></span> <br/> |
   

