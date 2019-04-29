---
title: '[X Justify] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: '[x] セルと [Y] セルによって定義された点に対する、アクションタグボタンの x 座標のオフセット値です。'
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414124"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="151f7-103">[X Justify] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="151f7-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="151f7-104">[x] セルと [Y] セルによって定義された点に対する、アクションタグボタンの*x*座標のオフセット値です。</span><span class="sxs-lookup"><span data-stu-id="151f7-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="151f7-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="151f7-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="151f7-106">**値**</span><span class="sxs-lookup"><span data-stu-id="151f7-106">**Value**</span></span>|<span data-ttu-id="151f7-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="151f7-107">**Description**</span></span>|<span data-ttu-id="151f7-108">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="151f7-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="151f7-109">.0</span><span class="sxs-lookup"><span data-stu-id="151f7-109">0</span></span>  <br/> | <span data-ttu-id="151f7-110">左揃えします (既定値)。</span><span class="sxs-lookup"><span data-stu-id="151f7-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="151f7-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="151f7-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="151f7-112">1 </span><span class="sxs-lookup"><span data-stu-id="151f7-112">1</span></span>  <br/> | <span data-ttu-id="151f7-113">中央揃え</span><span class="sxs-lookup"><span data-stu-id="151f7-113">Centered.</span></span>  <br/> |<span data-ttu-id="151f7-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="151f7-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="151f7-115">2 </span><span class="sxs-lookup"><span data-stu-id="151f7-115">2</span></span>  <br/> | <span data-ttu-id="151f7-116">右揃えします。</span><span class="sxs-lookup"><span data-stu-id="151f7-116">Right justified.</span></span>  <br/> |<span data-ttu-id="151f7-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="151f7-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="151f7-118">注釈</span><span class="sxs-lookup"><span data-stu-id="151f7-118">Remarks</span></span>

<span data-ttu-id="151f7-119">[x justify] セルと [y justify] セルは、[x] セルと [y] セルで定義されている点に対して、アクションタグボタンが配置される場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="151f7-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="151f7-120">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [X Justify] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="151f7-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="151f7-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="151f7-121">Cell name:</span></span>  <br/> | <span data-ttu-id="151f7-122">タグ.</span><span class="sxs-lookup"><span data-stu-id="151f7-122">SmartTags.</span></span>  <span data-ttu-id="151f7-123">*名前*です。xjustify (SmartTags)</span><span class="sxs-lookup"><span data-stu-id="151f7-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="151f7-124">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="151f7-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="151f7-125">プログラムから、インデックスによって [X Justify] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="151f7-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="151f7-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="151f7-126">Section index:</span></span>  <br/> |<span data-ttu-id="151f7-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="151f7-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="151f7-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="151f7-128">Row index:</span></span>  <br/> |<span data-ttu-id="151f7-129">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="151f7-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="151f7-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="151f7-130">Cell index:</span></span>  <br/> |<span data-ttu-id="151f7-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="151f7-131">**visSmartTagXJustify**</span></span> <br/> |
   

