---
title: DisplayMode セル (アクション タグのセクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: アクションのタグには、ユーザーがタグの上、ポインターを移動すると、図形が選択されている場合、またはすべての時間が表示されるかどうかを決定します。
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805219"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="37573-103">DisplayMode セル (アクション タグのセクション)</span><span class="sxs-lookup"><span data-stu-id="37573-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="37573-104">アクションのタグには、ユーザーがタグの上、ポインターを移動すると、図形が選択されている場合、またはすべての時間が表示されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="37573-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="37573-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="37573-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="37573-106">**値**</span><span class="sxs-lookup"><span data-stu-id="37573-106">**Value**</span></span>|<span data-ttu-id="37573-107">**表示モード**</span><span class="sxs-lookup"><span data-stu-id="37573-107">**Display Mode**</span></span>|<span data-ttu-id="37573-108">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="37573-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="37573-109">0</span><span class="sxs-lookup"><span data-stu-id="37573-109">0</span></span>  <br/> | <span data-ttu-id="37573-110">タグ (デフォルト) の上にマウスを置いたときに表示されます。</span><span class="sxs-lookup"><span data-stu-id="37573-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="37573-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="37573-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="37573-112">1</span><span class="sxs-lookup"><span data-stu-id="37573-112">1</span></span>  <br/> | <span data-ttu-id="37573-113">図形を選択したときに表示します。</span><span class="sxs-lookup"><span data-stu-id="37573-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="37573-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="37573-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="37573-115">2</span><span class="sxs-lookup"><span data-stu-id="37573-115">2</span></span>  <br/> | <span data-ttu-id="37573-116">常に表示します。</span><span class="sxs-lookup"><span data-stu-id="37573-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="37573-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="37573-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37573-118">備考</span><span class="sxs-lookup"><span data-stu-id="37573-118">Remarks</span></span>

<span data-ttu-id="37573-119">アクション タグは、印刷時や発行時には表示されません。</span><span class="sxs-lookup"><span data-stu-id="37573-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="37573-120">ページに対してアクション タグが定義されていて、このセルの値が 1 の場合、ページは選択できないためタグは表示されません。</span><span class="sxs-lookup"><span data-stu-id="37573-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="37573-121">取得する DisplayMode] セルへの参照の名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="37573-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37573-122">セル名:</span><span class="sxs-lookup"><span data-stu-id="37573-122">Cell name:</span></span>  <br/> | <span data-ttu-id="37573-123">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="37573-123">SmartTags.</span></span>  <span data-ttu-id="37573-124">*名*です。DisplayMode、スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="37573-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="37573-125">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="37573-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="37573-126">プログラムから、インデックスによって [DisplayMode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="37573-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37573-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="37573-127">Section index:</span></span>  <br/> |<span data-ttu-id="37573-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="37573-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="37573-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="37573-129">Row index:</span></span>  <br/> |<span data-ttu-id="37573-130">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="37573-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="37573-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="37573-131">Cell index:</span></span>  <br/> |<span data-ttu-id="37573-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="37573-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

