---
title: '[TheText] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: 図形のテキストまたはテキストの構成が変更されたときに評価されるイベント セルです。
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326678"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="62bbc-103">[TheText] セル ([Events] セクション)</span><span class="sxs-lookup"><span data-stu-id="62bbc-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="62bbc-104">図形のテキストまたはテキストの構成が変更されたときに評価されるイベント セルです。</span><span class="sxs-lookup"><span data-stu-id="62bbc-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62bbc-105">解説</span><span class="sxs-lookup"><span data-stu-id="62bbc-105">Remarks</span></span>

<span data-ttu-id="62bbc-p101">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。[TheText] セルを使用して、再計算をトリガーできます。たとえば TEXTWIDTH( ) および TEXTHEIGHT( ) 関数を使用してテキストの幅と高さを再計算できます。</span><span class="sxs-lookup"><span data-stu-id="62bbc-p101">Event cells are evaluated only when the event occurs, not upon formula entry. You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="62bbc-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TheText] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="62bbc-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62bbc-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="62bbc-109">Cell name:</span></span>  <br/> | <span data-ttu-id="62bbc-110">[thetext]</span><span class="sxs-lookup"><span data-stu-id="62bbc-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="62bbc-111">プログラムから、インデックスによって [TheText] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="62bbc-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62bbc-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="62bbc-112">Section index:</span></span>  <br/> |<span data-ttu-id="62bbc-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="62bbc-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="62bbc-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="62bbc-114">Row index:</span></span>  <br/> |<span data-ttu-id="62bbc-115">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="62bbc-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="62bbc-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="62bbc-116">Cell index:</span></span>  <br/> |<span data-ttu-id="62bbc-117">**visEvtCellTheText**</span><span class="sxs-lookup"><span data-stu-id="62bbc-117">**visEvtCellTheText**</span></span> <br/> |
   

