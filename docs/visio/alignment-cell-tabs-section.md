---
title: '[Alignment] セル ([Tabs] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: タブの整列方法を指定します。
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341539"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="1bd99-103">[Alignment] セル ([Tabs] セクション)</span><span class="sxs-lookup"><span data-stu-id="1bd99-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="1bd99-104">タブの整列方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="1bd99-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="1bd99-105">**値**</span><span class="sxs-lookup"><span data-stu-id="1bd99-105">**Value**</span></span>|<span data-ttu-id="1bd99-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="1bd99-106">**Alignment**</span></span>|<span data-ttu-id="1bd99-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="1bd99-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1bd99-108">.0</span><span class="sxs-lookup"><span data-stu-id="1bd99-108">0</span></span>  <br/> | <span data-ttu-id="1bd99-109">Left</span><span class="sxs-lookup"><span data-stu-id="1bd99-109">Left</span></span>  <br/> |<span data-ttu-id="1bd99-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="1bd99-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="1bd99-111">1-d</span><span class="sxs-lookup"><span data-stu-id="1bd99-111">1</span></span>  <br/> | <span data-ttu-id="1bd99-112">中央</span><span class="sxs-lookup"><span data-stu-id="1bd99-112">Center</span></span>  <br/> |<span data-ttu-id="1bd99-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="1bd99-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="1bd99-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="1bd99-114">2</span></span>  <br/> | <span data-ttu-id="1bd99-115">右</span><span class="sxs-lookup"><span data-stu-id="1bd99-115">Right</span></span>  <br/> |<span data-ttu-id="1bd99-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="1bd99-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="1bd99-117">1/3</span><span class="sxs-lookup"><span data-stu-id="1bd99-117">3</span></span>  <br/> | <span data-ttu-id="1bd99-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="1bd99-118">Decimal</span></span>  <br/> |<span data-ttu-id="1bd99-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="1bd99-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="1bd99-120">2/4</span><span class="sxs-lookup"><span data-stu-id="1bd99-120">4</span></span>  <br/> | <span data-ttu-id="1bd99-121">カンマ</span><span class="sxs-lookup"><span data-stu-id="1bd99-121">Comma</span></span>  <br/> |<span data-ttu-id="1bd99-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="1bd99-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bd99-123">解説</span><span class="sxs-lookup"><span data-stu-id="1bd99-123">Remarks</span></span>

<span data-ttu-id="1bd99-124">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Alignment] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd99-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1bd99-125">セル名 :</span><span class="sxs-lookup"><span data-stu-id="1bd99-125">Cell name:</span></span>  <br/> | <span data-ttu-id="1bd99-126">タブ.</span><span class="sxs-lookup"><span data-stu-id="1bd99-126">Tabs.</span></span>  <span data-ttu-id="1bd99-127">*ij* where *i および j =* <1>、2、3</span><span class="sxs-lookup"><span data-stu-id="1bd99-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="1bd99-128">プログラムから、インデックスによって [Alignment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1bd99-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1bd99-129">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1bd99-129">Section index:</span></span>  <br/> |<span data-ttu-id="1bd99-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="1bd99-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="1bd99-131">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1bd99-131">Row index:</span></span>  <br/> |<span data-ttu-id="1bd99-132">\*\*visRowTab +\*\*\*\* i = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="1bd99-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1bd99-133">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1bd99-133">Cell index:</span></span>  <br/> | <span data-ttu-id="1bd99-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="1bd99-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

