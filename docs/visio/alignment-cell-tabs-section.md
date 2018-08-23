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
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804762"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="eeec8-103">[Alignment] セル ([タブ] セクション)</span><span class="sxs-lookup"><span data-stu-id="eeec8-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="eeec8-104">タブの整列方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="eeec8-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="eeec8-105">**値**</span><span class="sxs-lookup"><span data-stu-id="eeec8-105">**Value**</span></span>|<span data-ttu-id="eeec8-106">**配置**</span><span class="sxs-lookup"><span data-stu-id="eeec8-106">**Alignment**</span></span>|<span data-ttu-id="eeec8-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="eeec8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="eeec8-108">0</span><span class="sxs-lookup"><span data-stu-id="eeec8-108">0</span></span>  <br/> | <span data-ttu-id="eeec8-109">左</span><span class="sxs-lookup"><span data-stu-id="eeec8-109">Left</span></span>  <br/> |<span data-ttu-id="eeec8-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="eeec8-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="eeec8-111">1</span><span class="sxs-lookup"><span data-stu-id="eeec8-111">1</span></span>  <br/> | <span data-ttu-id="eeec8-112">中央揃え</span><span class="sxs-lookup"><span data-stu-id="eeec8-112">Center</span></span>  <br/> |<span data-ttu-id="eeec8-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="eeec8-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="eeec8-114">2</span><span class="sxs-lookup"><span data-stu-id="eeec8-114">2</span></span>  <br/> | <span data-ttu-id="eeec8-115">右</span><span class="sxs-lookup"><span data-stu-id="eeec8-115">Right</span></span>  <br/> |<span data-ttu-id="eeec8-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="eeec8-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="eeec8-117">3</span><span class="sxs-lookup"><span data-stu-id="eeec8-117">3</span></span>  <br/> | <span data-ttu-id="eeec8-118">小数</span><span class="sxs-lookup"><span data-stu-id="eeec8-118">Decimal</span></span>  <br/> |<span data-ttu-id="eeec8-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="eeec8-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="eeec8-120">4</span><span class="sxs-lookup"><span data-stu-id="eeec8-120">4</span></span>  <br/> | <span data-ttu-id="eeec8-121">カンマ</span><span class="sxs-lookup"><span data-stu-id="eeec8-121">Comma</span></span>  <br/> |<span data-ttu-id="eeec8-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="eeec8-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eeec8-123">注釈</span><span class="sxs-lookup"><span data-stu-id="eeec8-123">Remarks</span></span>

<span data-ttu-id="eeec8-124">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Alignment] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="eeec8-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eeec8-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="eeec8-125">Cell name:</span></span>  <br/> | <span data-ttu-id="eeec8-126">タブします。</span><span class="sxs-lookup"><span data-stu-id="eeec8-126">Tabs.</span></span>  <span data-ttu-id="eeec8-127">*ij* *i および j =* < 1 > では、2、3</span><span class="sxs-lookup"><span data-stu-id="eeec8-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="eeec8-128">プログラムから、インデックスによって [Alignment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eeec8-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eeec8-129">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eeec8-129">Section index:</span></span>  <br/> |<span data-ttu-id="eeec8-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="eeec8-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="eeec8-131">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="eeec8-131">Row index:</span></span>  <br/> |<span data-ttu-id="eeec8-132">**visRowTab +***i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="eeec8-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="eeec8-133">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eeec8-133">Cell index:</span></span>  <br/> | <span data-ttu-id="eeec8-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="eeec8-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

