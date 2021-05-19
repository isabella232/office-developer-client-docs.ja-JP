---
title: '[SortKey] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: ショートカット メニューまたはアクション タグ メニューに表示されるアクションの順序を指定する数字です。
ms.openlocfilehash: d4eb98055f199f603003b068dca9fa7b4e377e52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419661"
---
# <a name="sortkey-cell-actions-section"></a><span data-ttu-id="418d5-103">[SortKey] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="418d5-103">SortKey Cell (Actions Section)</span></span>

<span data-ttu-id="418d5-104">ショートカット メニューまたはアクション タグ メニューに表示されるアクションの順序を指定する数字です。</span><span class="sxs-lookup"><span data-stu-id="418d5-104">A number that determines the order of actions that appear on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="418d5-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="418d5-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="418d5-106">注釈</span><span class="sxs-lookup"><span data-stu-id="418d5-106">Remarks</span></span>

<span data-ttu-id="418d5-p101">ショートカット メニューまたはアクション タグ メニューのアクションは、最小の数値から最大の数値の順に並べられ、最小の数値がメニューの一番上に表示されます。2 つのアクション行で [SortKey] セルの値が同じ場合は、物理的な行の順序で並べられます。既定値は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="418d5-p101">The actions on an action tag or shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two action rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span>
  
<span data-ttu-id="418d5-110">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [SortKey] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="418d5-110">To get a reference to the SortKey cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="418d5-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="418d5-111">Cell name:</span></span>  <br/> |<span data-ttu-id="418d5-112">アクション。</span><span class="sxs-lookup"><span data-stu-id="418d5-112">Actions.</span></span> <span data-ttu-id="418d5-113">*name*  .SortKeywhere アクション。</span><span class="sxs-lookup"><span data-stu-id="418d5-113">*name*  .SortKeywhere Actions.</span></span>  <span data-ttu-id="418d5-114">*name*  は [アクション] 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="418d5-114">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="418d5-115">プログラムから、インデックスによって [SortKey] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="418d5-115">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="418d5-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="418d5-116">Section index:</span></span>  <br/> |<span data-ttu-id="418d5-117">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="418d5-117">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="418d5-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="418d5-118">Row index:</span></span>  <br/> |<span data-ttu-id="418d5-119">**visRowAction**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="418d5-119">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="418d5-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="418d5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="418d5-121">**visActionSortKey**</span><span class="sxs-lookup"><span data-stu-id="418d5-121">**visActionSortKey**</span></span> <br/> |
   

