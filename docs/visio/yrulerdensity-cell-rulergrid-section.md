---
title: YRulerDensity セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: ページのルーラーに対して、垂直方向の小区分を指定します。
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806845"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="03fbc-103">YRulerDensity セル (ルーラー&amp;グリッド セクション)</span><span class="sxs-lookup"><span data-stu-id="03fbc-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="03fbc-104">ページのルーラーに対して、垂直方向の小区分を指定します。</span><span class="sxs-lookup"><span data-stu-id="03fbc-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="03fbc-105">**値**</span><span class="sxs-lookup"><span data-stu-id="03fbc-105">**Value**</span></span>|<span data-ttu-id="03fbc-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="03fbc-106">**Description**</span></span>|<span data-ttu-id="03fbc-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="03fbc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03fbc-108">0</span><span class="sxs-lookup"><span data-stu-id="03fbc-108">0</span></span>  <br/> |<span data-ttu-id="03fbc-109">固定</span><span class="sxs-lookup"><span data-stu-id="03fbc-109">Fixed</span></span>  <br/> |<span data-ttu-id="03fbc-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="03fbc-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="03fbc-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="03fbc-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="03fbc-112">粗い</span><span class="sxs-lookup"><span data-stu-id="03fbc-112">Coarse</span></span>  <br/> |<span data-ttu-id="03fbc-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="03fbc-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="03fbc-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="03fbc-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="03fbc-115">標準 (既定値)</span><span class="sxs-lookup"><span data-stu-id="03fbc-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="03fbc-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="03fbc-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="03fbc-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="03fbc-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="03fbc-118">細かい</span><span class="sxs-lookup"><span data-stu-id="03fbc-118">Fine</span></span>  <br/> |<span data-ttu-id="03fbc-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="03fbc-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03fbc-120">備考</span><span class="sxs-lookup"><span data-stu-id="03fbc-120">Remarks</span></span>

<span data-ttu-id="03fbc-121">このセル内の垂直方向の**目盛り**] オプションに対応して、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。</span><span class="sxs-lookup"><span data-stu-id="03fbc-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="03fbc-122">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[YRulerDensity] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="03fbc-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03fbc-123">セル名 :</span><span class="sxs-lookup"><span data-stu-id="03fbc-123">Cell name:</span></span>  <br/> |<span data-ttu-id="03fbc-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="03fbc-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="03fbc-125">プログラムから、インデックスによって [YRulerDensity] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="03fbc-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03fbc-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="03fbc-126">Section index:</span></span>  <br/> |<span data-ttu-id="03fbc-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="03fbc-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="03fbc-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="03fbc-128">Row index:</span></span>  <br/> |<span data-ttu-id="03fbc-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="03fbc-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="03fbc-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="03fbc-130">Cell index:</span></span>  <br/> |<span data-ttu-id="03fbc-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="03fbc-131">**visYRulerDensity**</span></span> <br/> |
   

