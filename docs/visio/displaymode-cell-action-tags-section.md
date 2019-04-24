---
title: DisplayMode セル (Action Tags セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: ユーザーがタグの上にポインターを移動したとき、図形を選択したとき、または常に [アクション] タグを表示するかどうかを指定します。
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332733"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="bd5f9-103">DisplayMode セル (Action Tags セクション)</span><span class="sxs-lookup"><span data-stu-id="bd5f9-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="bd5f9-104">ユーザーがタグの上にポインターを移動したとき、図形を選択したとき、または常に [アクション] タグを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bd5f9-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="bd5f9-106">**値**</span><span class="sxs-lookup"><span data-stu-id="bd5f9-106">**Value**</span></span>|<span data-ttu-id="bd5f9-107">**表示モード**</span><span class="sxs-lookup"><span data-stu-id="bd5f9-107">**Display Mode**</span></span>|<span data-ttu-id="bd5f9-108">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="bd5f9-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="bd5f9-109">.0</span><span class="sxs-lookup"><span data-stu-id="bd5f9-109">0</span></span>  <br/> | <span data-ttu-id="bd5f9-110">タグ上でマウスを一時停止したときに表示されます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="bd5f9-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="bd5f9-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="bd5f9-112">1-d</span><span class="sxs-lookup"><span data-stu-id="bd5f9-112">1</span></span>  <br/> | <span data-ttu-id="bd5f9-113">図形を選択したときに表示します。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="bd5f9-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="bd5f9-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="bd5f9-115">pbm-2</span><span class="sxs-lookup"><span data-stu-id="bd5f9-115">2</span></span>  <br/> | <span data-ttu-id="bd5f9-116">常に表示します。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="bd5f9-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="bd5f9-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd5f9-118">解説</span><span class="sxs-lookup"><span data-stu-id="bd5f9-118">Remarks</span></span>

<span data-ttu-id="bd5f9-119">アクション タグは、印刷時や発行時には表示されません。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="bd5f9-120">ページに対してアクション タグが定義されていて、このセルの値が 1 の場合、ページは選択できないためタグは表示されません。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="bd5f9-121">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [DisplayMode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd5f9-122">セル名:</span><span class="sxs-lookup"><span data-stu-id="bd5f9-122">Cell name:</span></span>  <br/> | <span data-ttu-id="bd5f9-123">タグ.</span><span class="sxs-lookup"><span data-stu-id="bd5f9-123">SmartTags.</span></span>  <span data-ttu-id="bd5f9-124">*名前*です。DisplayMode の場合は、SmartTags。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="bd5f9-125">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="bd5f9-126">プログラムから、インデックスによって [DisplayMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd5f9-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd5f9-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd5f9-127">Section index:</span></span>  <br/> |<span data-ttu-id="bd5f9-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="bd5f9-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="bd5f9-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd5f9-129">Row index:</span></span>  <br/> |<span data-ttu-id="bd5f9-130">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="bd5f9-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bd5f9-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd5f9-131">Cell index:</span></span>  <br/> |<span data-ttu-id="bd5f9-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="bd5f9-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

