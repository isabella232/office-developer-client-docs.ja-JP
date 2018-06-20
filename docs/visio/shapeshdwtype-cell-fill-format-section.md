---
title: '[ShapeShdwType] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: 図形の影の種類を指定します。
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806418"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="49ca2-103">[ShapeShdwType] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="49ca2-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="49ca2-104">図形の影の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="49ca2-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="49ca2-105">**値**</span><span class="sxs-lookup"><span data-stu-id="49ca2-105">**Value**</span></span>|<span data-ttu-id="49ca2-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="49ca2-106">**Description**</span></span>|<span data-ttu-id="49ca2-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="49ca2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="49ca2-108">0</span><span class="sxs-lookup"><span data-stu-id="49ca2-108">0</span></span>  <br/> |<span data-ttu-id="49ca2-109">ページの既定値を使用します (既定値)。</span><span class="sxs-lookup"><span data-stu-id="49ca2-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="49ca2-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="49ca2-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="49ca2-111">1</span><span class="sxs-lookup"><span data-stu-id="49ca2-111">1</span></span>  <br/> |<span data-ttu-id="49ca2-112">シンプルな影です。</span><span class="sxs-lookup"><span data-stu-id="49ca2-112">Simple</span></span>  <br/> |<span data-ttu-id="49ca2-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="49ca2-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="49ca2-114">2</span><span class="sxs-lookup"><span data-stu-id="49ca2-114">2</span></span>  <br/> |<span data-ttu-id="49ca2-115">斜体の影です。</span><span class="sxs-lookup"><span data-stu-id="49ca2-115">Oblique</span></span>  <br/> |<span data-ttu-id="49ca2-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="49ca2-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49ca2-117">備考</span><span class="sxs-lookup"><span data-stu-id="49ca2-117">Remarks</span></span>

<span data-ttu-id="49ca2-118">(デフォルト ページの影の種類は [ページ プロパティ] セクションの [shdwtype] セルで定義されている) ページの既定値とは異なる図形の影を適用するのにには、このセルを使用します。</span><span class="sxs-lookup"><span data-stu-id="49ca2-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="49ca2-119">シンプルな影は、ユーザー インターフェイス (UI) 内のオフセットの影として説明します。</span><span class="sxs-lookup"><span data-stu-id="49ca2-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="49ca2-120">シンプルな影は図形の背後にある平行な平面上にシャドウされている図形の効果を示します。</span><span class="sxs-lookup"><span data-stu-id="49ca2-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="49ca2-121">斜体の影は、UI 内の斜体の影として説明され、図形に垂直な平面に影の効果を与えます。</span><span class="sxs-lookup"><span data-stu-id="49ca2-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="49ca2-122">事前定義された単純な影と斜体の影の一覧で、[**影**] ダイアログ ボックスの [**スタイル**] ボックスを参照してください ([**ホーム**] タブの [**図形**] グループで、**シャドウ**] をクリックし、[**影のオプション**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="49ca2-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="49ca2-123">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapeShdwType] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="49ca2-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49ca2-124">セル名 :</span><span class="sxs-lookup"><span data-stu-id="49ca2-124">Cell name:</span></span>  <br/> |<span data-ttu-id="49ca2-125">ShapeShdwType</span><span class="sxs-lookup"><span data-stu-id="49ca2-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="49ca2-126">プログラムから、インデックスによって [ShapeShdwType] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="49ca2-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49ca2-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="49ca2-127">Section index:</span></span>  <br/> |<span data-ttu-id="49ca2-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="49ca2-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="49ca2-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="49ca2-129">Row index:</span></span>  <br/> |<span data-ttu-id="49ca2-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="49ca2-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="49ca2-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="49ca2-131">Cell index:</span></span>  <br/> |<span data-ttu-id="49ca2-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="49ca2-132">**visFillShdwType**</span></span> <br/> |
   

