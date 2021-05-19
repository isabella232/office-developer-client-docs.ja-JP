---
title: '[ShdwType] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: ページの既定の影の種類を指定します。
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424099"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="ea9e9-103">[ShdwType] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="ea9e9-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="ea9e9-104">ページの既定の影の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea9e9-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="ea9e9-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ea9e9-105">**Value**</span></span>|<span data-ttu-id="ea9e9-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea9e9-106">**Description**</span></span>|<span data-ttu-id="ea9e9-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="ea9e9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ea9e9-108">1</span><span class="sxs-lookup"><span data-stu-id="ea9e9-108">1</span></span>  <br/> | <span data-ttu-id="ea9e9-109">シンプル</span><span class="sxs-lookup"><span data-stu-id="ea9e9-109">Simple</span></span>  <br/> |<span data-ttu-id="ea9e9-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="ea9e9-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="ea9e9-111">2</span><span class="sxs-lookup"><span data-stu-id="ea9e9-111">2</span></span>  <br/> | <span data-ttu-id="ea9e9-112">斜め</span><span class="sxs-lookup"><span data-stu-id="ea9e9-112">Oblique</span></span>  <br/> |<span data-ttu-id="ea9e9-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="ea9e9-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="ea9e9-114">3</span><span class="sxs-lookup"><span data-stu-id="ea9e9-114">3</span></span>  <br/> |<span data-ttu-id="ea9e9-115">Inner</span><span class="sxs-lookup"><span data-stu-id="ea9e9-115">Inner</span></span>  <br/> |<span data-ttu-id="ea9e9-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="ea9e9-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea9e9-117">注釈</span><span class="sxs-lookup"><span data-stu-id="ea9e9-117">Remarks</span></span>

 <span data-ttu-id="ea9e9-118">このセルで説明するシャドウの種類は、ShapeShdwType セル (ページ上の個々の図形のシャドウ の種類) が Page Default **(visFSTPageDefault)** に設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea9e9-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="ea9e9-119">シンプルな影は、ユーザー インターフェイス (UI) 内では "オフセット" と表示されます。</span><span class="sxs-lookup"><span data-stu-id="ea9e9-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="ea9e9-120">シンプルな影は、その図形の下の平面に影を落としているように見えます。</span><span class="sxs-lookup"><span data-stu-id="ea9e9-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="ea9e9-121">斜体の影は UI で "斜体" と表示され、図形が直立している平面に影を落としているように見えます。</span><span class="sxs-lookup"><span data-stu-id="ea9e9-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="ea9e9-122">定義済みのシンプルな影と斜体の影の一覧は、[**ページ設定**] ダイアログ ボックスの [**影**] タブにある [**スタイル**] ボックスの一覧を参照してください (このダイアログ ボックスを開くには、[**デザイン**] タブで、[**ページ設定**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="ea9e9-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="ea9e9-123">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwType] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ea9e9-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea9e9-124">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ea9e9-124">Cell name:</span></span>  <br/> | <span data-ttu-id="ea9e9-125">ShdwType</span><span class="sxs-lookup"><span data-stu-id="ea9e9-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="ea9e9-126">プログラムから、インデックスによって [ShapeShdwOffsetX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea9e9-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea9e9-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea9e9-127">Section index:</span></span>  <br/> |<span data-ttu-id="ea9e9-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ea9e9-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ea9e9-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea9e9-129">Row index:</span></span>  <br/> |<span data-ttu-id="ea9e9-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="ea9e9-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="ea9e9-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea9e9-131">Cell index:</span></span>  <br/> |<span data-ttu-id="ea9e9-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="ea9e9-132">**visPageShdwType**</span></span> <br/> |
   

