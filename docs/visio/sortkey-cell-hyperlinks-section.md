---
title: '[SortKey] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: ショートカット メニューに表示されるハイパーリンクの順序を特定する数です。
ms.openlocfilehash: 03596918924b04a776eb7ffd2f16db1c57de8194
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806547"
---
# <a name="sortkey-cell-hyperlinks-section"></a><span data-ttu-id="276bc-103">[SortKey] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="276bc-103">SortKey Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="276bc-104">ショートカット メニューに表示されるハイパーリンクの順序を特定する数です。</span><span class="sxs-lookup"><span data-stu-id="276bc-104">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="276bc-105">注釈</span><span class="sxs-lookup"><span data-stu-id="276bc-105">Remarks</span></span>

<span data-ttu-id="276bc-p101">ショートカット メニューのハイパーリンクは、昇順にソートされてメニューに表示されます。メニューの一番上には、最小の数値が表示されます。2 つのハイパーリンク行の [SortKey] セルの値が同じ場合、順番は物理的な行順序によって特定されます。既定値は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="276bc-p101">The hyperlinks on a shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two hyperlink rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span> 
  
<span data-ttu-id="276bc-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [sortkey] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="276bc-109">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="276bc-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="276bc-110">Cell name:</span></span>  <br/> |<span data-ttu-id="276bc-111">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="276bc-111">Hyperlink.</span></span> <span data-ttu-id="276bc-112">*名*です。[Sortkey] のハイパーリンクの *.name*と行の名前があります。</span><span class="sxs-lookup"><span data-stu-id="276bc-112">*name*  .SortKey where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="276bc-113">プログラムから、インデックスによって [sortkey] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="276bc-113">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="276bc-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="276bc-114">Section index:</span></span>  <br/> |<span data-ttu-id="276bc-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="276bc-115">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="276bc-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="276bc-116">Row index:</span></span>  <br/> |<span data-ttu-id="276bc-117">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="276bc-117">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="276bc-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="276bc-118">Cell index:</span></span>  <br/> |<span data-ttu-id="276bc-119">**visHLinkSortKey**</span><span class="sxs-lookup"><span data-stu-id="276bc-119">**visHLinkSortKey**</span></span> <br/> |
   
