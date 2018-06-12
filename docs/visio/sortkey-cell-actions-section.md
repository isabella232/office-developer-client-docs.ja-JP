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
ms.openlocfilehash: 5a5db1276d1f2544b5b2b76301c30a2bedd4be63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806562"
---
# <a name="sortkey-cell-actions-section"></a><span data-ttu-id="dc86b-103">[SortKey] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="dc86b-103">SortKey Cell (Actions Section)</span></span>

<span data-ttu-id="dc86b-104">ショートカット メニューまたはアクション タグ メニューに表示されるアクションの順序を指定する数字です。</span><span class="sxs-lookup"><span data-stu-id="dc86b-104">A number that determines the order of actions that appear on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dc86b-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="dc86b-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dc86b-106">注釈</span><span class="sxs-lookup"><span data-stu-id="dc86b-106">Remarks</span></span>

<span data-ttu-id="dc86b-p101">ショートカット メニューまたはアクション タグ メニューのアクションは、最小の数値から最大の数値の順に並べられ、最小の数値がメニューの一番上に表示されます。2 つのアクション行で [SortKey] セルの値が同じ場合は、物理的な行の順序で並べられます。既定値は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="dc86b-p101">The actions on an action tag or shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two action rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span>
  
<span data-ttu-id="dc86b-110">取得する [sortkey] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="dc86b-110">To get a reference to the SortKey cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc86b-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="dc86b-111">Cell name:</span></span>  <br/> |<span data-ttu-id="dc86b-112">アクションです。</span><span class="sxs-lookup"><span data-stu-id="dc86b-112">Actions.</span></span> <span data-ttu-id="dc86b-113">*名*です。SortKeywhere アクションです。</span><span class="sxs-lookup"><span data-stu-id="dc86b-113">*name*  .SortKeywhere Actions.</span></span>  <span data-ttu-id="dc86b-114">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="dc86b-114">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="dc86b-115">プログラムから、インデックスによって [sortkey] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="dc86b-115">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc86b-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dc86b-116">Section index:</span></span>  <br/> |<span data-ttu-id="dc86b-117">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="dc86b-117">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="dc86b-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dc86b-118">Row index:</span></span>  <br/> |<span data-ttu-id="dc86b-119">**visRowAction** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="dc86b-119">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="dc86b-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dc86b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dc86b-121">**visActionSortKey**</span><span class="sxs-lookup"><span data-stu-id="dc86b-121">**visActionSortKey**</span></span> <br/> |
   
