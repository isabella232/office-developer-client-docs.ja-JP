---
title: '[Y Justify] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Y、X と Y セルによって定義された点を基準にして、操作タグ ボタンのオフセット。
ms.openlocfilehash: 8f8323d1f392654bf118ece2f78890f2a1b860ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806842"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="0d827-103">[Y Justify] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="0d827-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="0d827-104">*Y* X と Y セルによって定義された点を基準にして、操作タグ ボタンのオフセット。</span><span class="sxs-lookup"><span data-stu-id="0d827-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0d827-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="0d827-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="0d827-106">**値**</span><span class="sxs-lookup"><span data-stu-id="0d827-106">**Value**</span></span>|<span data-ttu-id="0d827-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d827-107">**Description**</span></span>|<span data-ttu-id="0d827-108">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="0d827-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0d827-109">0</span><span class="sxs-lookup"><span data-stu-id="0d827-109">0</span></span>  <br/> | <span data-ttu-id="0d827-110">上揃えします (既定値)。</span><span class="sxs-lookup"><span data-stu-id="0d827-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="0d827-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="0d827-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="0d827-112">1</span><span class="sxs-lookup"><span data-stu-id="0d827-112">1</span></span>  <br/> | <span data-ttu-id="0d827-113">中央揃え</span><span class="sxs-lookup"><span data-stu-id="0d827-113">Centered.</span></span>  <br/> |<span data-ttu-id="0d827-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="0d827-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="0d827-115">2</span><span class="sxs-lookup"><span data-stu-id="0d827-115">2</span></span>  <br/> | <span data-ttu-id="0d827-116">下揃えします。</span><span class="sxs-lookup"><span data-stu-id="0d827-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="0d827-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="0d827-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d827-118">備考</span><span class="sxs-lookup"><span data-stu-id="0d827-118">Remarks</span></span>

<span data-ttu-id="0d827-119">X Justify] および [Y Justify] の各セルは、X と Y のセルで定義されているポイントを基準にして、操作タグ ボタンを配置する場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="0d827-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="0d827-120">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Y Justify] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="0d827-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d827-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="0d827-121">Cell name:</span></span>  <br/> | <span data-ttu-id="0d827-122">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="0d827-122">SmartTags.</span></span>  <span data-ttu-id="0d827-123">*名*です。YJustify、スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="0d827-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="0d827-124">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="0d827-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="0d827-125">プログラムから、インデックスによって [Y Justify] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d827-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d827-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d827-126">Section index:</span></span>  <br/> |<span data-ttu-id="0d827-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="0d827-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="0d827-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d827-128">Row index:</span></span>  <br/> |<span data-ttu-id="0d827-129">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="0d827-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0d827-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d827-130">Cell index:</span></span>  <br/> |<span data-ttu-id="0d827-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="0d827-131">**visSmartTagYJustify**</span></span> <br/> |
   

