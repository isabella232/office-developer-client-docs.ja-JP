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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425541"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="9b53a-103">[Alignment] セル ([Tabs] セクション)</span><span class="sxs-lookup"><span data-stu-id="9b53a-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="9b53a-104">タブの整列方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b53a-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="9b53a-105">**値**</span><span class="sxs-lookup"><span data-stu-id="9b53a-105">**Value**</span></span>|<span data-ttu-id="9b53a-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="9b53a-106">**Alignment**</span></span>|<span data-ttu-id="9b53a-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="9b53a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9b53a-108">0</span><span class="sxs-lookup"><span data-stu-id="9b53a-108">0</span></span>  <br/> | <span data-ttu-id="9b53a-109">Left</span><span class="sxs-lookup"><span data-stu-id="9b53a-109">Left</span></span>  <br/> |<span data-ttu-id="9b53a-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="9b53a-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="9b53a-111">1</span><span class="sxs-lookup"><span data-stu-id="9b53a-111">1</span></span>  <br/> | <span data-ttu-id="9b53a-112">中央</span><span class="sxs-lookup"><span data-stu-id="9b53a-112">Center</span></span>  <br/> |<span data-ttu-id="9b53a-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="9b53a-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="9b53a-114">2</span><span class="sxs-lookup"><span data-stu-id="9b53a-114">2</span></span>  <br/> | <span data-ttu-id="9b53a-115">右</span><span class="sxs-lookup"><span data-stu-id="9b53a-115">Right</span></span>  <br/> |<span data-ttu-id="9b53a-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="9b53a-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="9b53a-117">3</span><span class="sxs-lookup"><span data-stu-id="9b53a-117">3</span></span>  <br/> | <span data-ttu-id="9b53a-118">10 進数</span><span class="sxs-lookup"><span data-stu-id="9b53a-118">Decimal</span></span>  <br/> |<span data-ttu-id="9b53a-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="9b53a-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="9b53a-120">4</span><span class="sxs-lookup"><span data-stu-id="9b53a-120">4</span></span>  <br/> | <span data-ttu-id="9b53a-121">カンマ</span><span class="sxs-lookup"><span data-stu-id="9b53a-121">Comma</span></span>  <br/> |<span data-ttu-id="9b53a-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="9b53a-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b53a-123">注釈</span><span class="sxs-lookup"><span data-stu-id="9b53a-123">Remarks</span></span>

<span data-ttu-id="9b53a-124">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Alignment] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b53a-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b53a-125">セル名 :</span><span class="sxs-lookup"><span data-stu-id="9b53a-125">Cell name:</span></span>  <br/> | <span data-ttu-id="9b53a-126">タブ。</span><span class="sxs-lookup"><span data-stu-id="9b53a-126">Tabs.</span></span>  <span data-ttu-id="9b53a-127">*ij*            は  *i と j = <*  1>、2、3</span><span class="sxs-lookup"><span data-stu-id="9b53a-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="9b53a-128">プログラムから、インデックスによって [Alignment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b53a-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b53a-129">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9b53a-129">Section index:</span></span>  <br/> |<span data-ttu-id="9b53a-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="9b53a-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="9b53a-131">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9b53a-131">Row index:</span></span>  <br/> |<span data-ttu-id="9b53a-132">**visRowTab +** *i*            *=*  0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9b53a-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9b53a-133">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9b53a-133">Cell index:</span></span>  <br/> | <span data-ttu-id="9b53a-134">(*j*  \*3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="9b53a-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

