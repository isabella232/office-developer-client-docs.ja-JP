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
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806467"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="2e4a3-103">[ShdwType] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="2e4a3-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="2e4a3-104">ページの既定の影の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="2e4a3-105">**値**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-105">**Value**</span></span>|<span data-ttu-id="2e4a3-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-106">**Description**</span></span>|<span data-ttu-id="2e4a3-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2e4a3-108">1</span><span class="sxs-lookup"><span data-stu-id="2e4a3-108">1</span></span>  <br/> | <span data-ttu-id="2e4a3-109">シンプルな影です。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-109">Simple</span></span>  <br/> |<span data-ttu-id="2e4a3-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="2e4a3-111">2</span><span class="sxs-lookup"><span data-stu-id="2e4a3-111">2</span></span>  <br/> | <span data-ttu-id="2e4a3-112">斜体の影です。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-112">Oblique</span></span>  <br/> |<span data-ttu-id="2e4a3-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="2e4a3-114">3</span><span class="sxs-lookup"><span data-stu-id="2e4a3-114">3</span></span>  <br/> |<span data-ttu-id="2e4a3-115">内部</span><span class="sxs-lookup"><span data-stu-id="2e4a3-115">Inner</span></span>  <br/> |<span data-ttu-id="2e4a3-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e4a3-117">備考</span><span class="sxs-lookup"><span data-stu-id="2e4a3-117">Remarks</span></span>

 <span data-ttu-id="2e4a3-118">ShapeShdwType セル (ページ上の個々 の図形の影の種類) がページの既定値 (**visFSTPageDefault** ) に設定するたびに、このセルに記載されている影の種類が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="2e4a3-119">シンプルな影は、ユーザー インターフェイス (UI) 内のオフセットの影として説明します。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="2e4a3-120">シンプルな影は、その背後にある程度の距離の平面上にシャドウされている図形の効果を示します。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="2e4a3-121">斜体の影は、UI 内の斜体の影として説明され、図形に垂直な平面に影の効果を与えます。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="2e4a3-122">事前定義された単純な影と斜体の影の一覧を参照してください**スタイル**] ボックスの一覧で、[**ページ設定**] ダイアログ ボックスの [**影**] タブ ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="2e4a3-123">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [shdwtype] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e4a3-124">セル名 :</span><span class="sxs-lookup"><span data-stu-id="2e4a3-124">Cell name:</span></span>  <br/> | <span data-ttu-id="2e4a3-125">[Shdwtype]</span><span class="sxs-lookup"><span data-stu-id="2e4a3-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="2e4a3-126">プログラムから、インデックスによって [ShapeShdwOffsetX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e4a3-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e4a3-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2e4a3-127">Section index:</span></span>  <br/> |<span data-ttu-id="2e4a3-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2e4a3-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2e4a3-129">Row index:</span></span>  <br/> |<span data-ttu-id="2e4a3-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="2e4a3-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2e4a3-131">Cell index:</span></span>  <br/> |<span data-ttu-id="2e4a3-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-132">**visPageShdwType**</span></span> <br/> |
   

