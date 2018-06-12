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
ms.openlocfilehash: 942ccee4478c87243207d8d65785857758d2a068
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806648"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="9f390-103">[TheText] セル ([Events] セクション)</span><span class="sxs-lookup"><span data-stu-id="9f390-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="9f390-104">図形のテキストまたはテキストの構成が変更されたときに評価されるイベント セルです。</span><span class="sxs-lookup"><span data-stu-id="9f390-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9f390-105">備考</span><span class="sxs-lookup"><span data-stu-id="9f390-105">Remarks</span></span>

<span data-ttu-id="9f390-p101">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。[TheText] セルを使用して、再計算をトリガーできます。たとえば TEXTWIDTH( ) および TEXTHEIGHT( ) 関数を使用してテキストの幅と高さを再計算できます。</span><span class="sxs-lookup"><span data-stu-id="9f390-p101">Event cells are evaluated only when the event occurs, not upon formula entry. You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="9f390-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [thetext] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="9f390-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f390-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="9f390-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9f390-110">テキスト</span><span class="sxs-lookup"><span data-stu-id="9f390-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="9f390-111">プログラムから、インデックスによって [thetext] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9f390-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f390-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9f390-112">Section index:</span></span>  <br/> |<span data-ttu-id="9f390-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9f390-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9f390-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9f390-114">Row index:</span></span>  <br/> |<span data-ttu-id="9f390-115">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="9f390-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="9f390-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9f390-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9f390-117">**visEvtCellTheText**</span><span class="sxs-lookup"><span data-stu-id="9f390-117">**visEvtCellTheText**</span></span> <br/> |
   

