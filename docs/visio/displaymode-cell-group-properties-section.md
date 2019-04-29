---
title: '[DisplayMode] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: グループ図形とそのメンバーの表示方法を指定します。
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413186"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="64169-103">[DisplayMode] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="64169-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="64169-104">グループ図形とそのメンバーの表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="64169-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="64169-105">**値**</span><span class="sxs-lookup"><span data-stu-id="64169-105">**Value**</span></span>|<span data-ttu-id="64169-106">**表示モード**</span><span class="sxs-lookup"><span data-stu-id="64169-106">**Display Mode**</span></span>|<span data-ttu-id="64169-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="64169-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="64169-108">.0</span><span class="sxs-lookup"><span data-stu-id="64169-108">0</span></span>  <br/> |<span data-ttu-id="64169-109">グループ図形とテキストを表示しません。</span><span class="sxs-lookup"><span data-stu-id="64169-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="64169-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="64169-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="64169-111">1 </span><span class="sxs-lookup"><span data-stu-id="64169-111">1</span></span>  <br/> |<span data-ttu-id="64169-112">メンバー図形の背後にグループ図形を表示します。</span><span class="sxs-lookup"><span data-stu-id="64169-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="64169-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="64169-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="64169-114">2 </span><span class="sxs-lookup"><span data-stu-id="64169-114">2</span></span>  <br/> |<span data-ttu-id="64169-115">メンバー図形の手前にグループ図形を表示します。</span><span class="sxs-lookup"><span data-stu-id="64169-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="64169-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="64169-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64169-117">注釈</span><span class="sxs-lookup"><span data-stu-id="64169-117">Remarks</span></span>

<span data-ttu-id="64169-118">この値を設定するには、グループを選択し、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで [**基本動作**] をクリックし、[**グループデータ**] ボックスの一覧から表示モードを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="64169-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="64169-119">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DisplayMode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="64169-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64169-120">セル名 :</span><span class="sxs-lookup"><span data-stu-id="64169-120">Cell name:</span></span>  <br/> |<span data-ttu-id="64169-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="64169-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="64169-122">プログラムから、インデックスによって [DisplayMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="64169-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64169-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="64169-123">Section index:</span></span>  <br/> |<span data-ttu-id="64169-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="64169-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="64169-125">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="64169-125">Row index:</span></span>  <br/> |<span data-ttu-id="64169-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="64169-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="64169-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="64169-127">Cell index:</span></span>  <br/> |<span data-ttu-id="64169-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="64169-128">**visGroupDisplayMode**</span></span> <br/> |
   

