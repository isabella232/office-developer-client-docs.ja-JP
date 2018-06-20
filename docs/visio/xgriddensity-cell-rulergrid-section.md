---
title: XGridDensity セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: 使用する水平方向のグリッドの種類を指定します。
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806817"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="c0ef4-103">XGridDensity セル (ルーラー&amp;グリッド セクション)</span><span class="sxs-lookup"><span data-stu-id="c0ef4-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="c0ef4-104">使用する水平方向のグリッドの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0ef4-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="c0ef4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-105">**Value**</span></span>|<span data-ttu-id="c0ef4-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-106">**Description**</span></span>|<span data-ttu-id="c0ef4-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0ef4-108">0</span><span class="sxs-lookup"><span data-stu-id="c0ef4-108">0</span></span>  <br/> |<span data-ttu-id="c0ef4-109">固定</span><span class="sxs-lookup"><span data-stu-id="c0ef4-109">Fixed</span></span>  <br/> |<span data-ttu-id="c0ef4-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="c0ef4-111">2</span><span class="sxs-lookup"><span data-stu-id="c0ef4-111">2</span></span>  <br/> |<span data-ttu-id="c0ef4-112">粗い</span><span class="sxs-lookup"><span data-stu-id="c0ef4-112">Coarse</span></span>  <br/> |<span data-ttu-id="c0ef4-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="c0ef4-114">4</span><span class="sxs-lookup"><span data-stu-id="c0ef4-114">4</span></span>  <br/> |<span data-ttu-id="c0ef4-115">標準 (既定値)</span><span class="sxs-lookup"><span data-stu-id="c0ef4-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="c0ef4-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="c0ef4-117">8</span><span class="sxs-lookup"><span data-stu-id="c0ef4-117">8</span></span>  <br/> |<span data-ttu-id="c0ef4-118">細かい</span><span class="sxs-lookup"><span data-stu-id="c0ef4-118">Fine</span></span>  <br/> |<span data-ttu-id="c0ef4-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0ef4-120">備考</span><span class="sxs-lookup"><span data-stu-id="c0ef4-120">Remarks</span></span>

<span data-ttu-id="c0ef4-121">このセルは、水平方向の**グリッド線の間隔**に対応するオプションで、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。</span><span class="sxs-lookup"><span data-stu-id="c0ef4-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="c0ef4-122">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[XGridDensity] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="c0ef4-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0ef4-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="c0ef4-123">Cell name:</span></span>  <br/> |<span data-ttu-id="c0ef4-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="c0ef4-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="c0ef4-125">プログラムから、インデックスによって [XGridDensity] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c0ef4-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0ef4-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c0ef4-126">Section index:</span></span>  <br/> |<span data-ttu-id="c0ef4-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c0ef4-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c0ef4-128">Row index:</span></span>  <br/> |<span data-ttu-id="c0ef4-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="c0ef4-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c0ef4-130">Cell index:</span></span>  <br/> |<span data-ttu-id="c0ef4-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="c0ef4-131">**visXGridDensity**</span></span> <br/> |
   

