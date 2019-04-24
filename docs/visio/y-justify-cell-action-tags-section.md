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
description: '[X] セルと [y] セルによって定義された点に対する、アクションタグボタンの y オフセット。'
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357016"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="0e962-103">[Y Justify] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="0e962-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="0e962-104">[X] セルと [y] セルによって定義された点に対する、アクションタグボタンの*y*オフセット。</span><span class="sxs-lookup"><span data-stu-id="0e962-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0e962-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="0e962-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="0e962-106">**値**</span><span class="sxs-lookup"><span data-stu-id="0e962-106">**Value**</span></span>|<span data-ttu-id="0e962-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="0e962-107">**Description**</span></span>|<span data-ttu-id="0e962-108">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="0e962-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0e962-109">.0</span><span class="sxs-lookup"><span data-stu-id="0e962-109">0</span></span>  <br/> | <span data-ttu-id="0e962-110">上揃えします (既定値)。</span><span class="sxs-lookup"><span data-stu-id="0e962-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="0e962-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="0e962-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="0e962-112">1-d</span><span class="sxs-lookup"><span data-stu-id="0e962-112">1</span></span>  <br/> | <span data-ttu-id="0e962-113">中央揃え</span><span class="sxs-lookup"><span data-stu-id="0e962-113">Centered.</span></span>  <br/> |<span data-ttu-id="0e962-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="0e962-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="0e962-115">pbm-2</span><span class="sxs-lookup"><span data-stu-id="0e962-115">2</span></span>  <br/> | <span data-ttu-id="0e962-116">下揃えします。</span><span class="sxs-lookup"><span data-stu-id="0e962-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="0e962-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="0e962-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e962-118">解説</span><span class="sxs-lookup"><span data-stu-id="0e962-118">Remarks</span></span>

<span data-ttu-id="0e962-119">[x justify] セルと [y justify] セルは、[x] セルと [y] セルで定義されている点に対して、アクションタグボタンが配置される場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="0e962-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="0e962-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Justify] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e962-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e962-121">セル名 :</span><span class="sxs-lookup"><span data-stu-id="0e962-121">Cell name:</span></span>  <br/> | <span data-ttu-id="0e962-122">タグ.</span><span class="sxs-lookup"><span data-stu-id="0e962-122">SmartTags.</span></span>  <span data-ttu-id="0e962-123">*名前*です。SmartTags の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e962-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="0e962-124">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="0e962-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="0e962-125">プログラムから、インデックスによって [Y Justify] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e962-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e962-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0e962-126">Section index:</span></span>  <br/> |<span data-ttu-id="0e962-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="0e962-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="0e962-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0e962-128">Row index:</span></span>  <br/> |<span data-ttu-id="0e962-129">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="0e962-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0e962-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0e962-130">Cell index:</span></span>  <br/> |<span data-ttu-id="0e962-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="0e962-131">**visSmartTagYJustify**</span></span> <br/> |
   

