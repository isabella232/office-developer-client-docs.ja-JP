---
title: '[PagesX] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: 図面ページに左右を揃えるプリンター ページの番号を指定します。
ms.openlocfilehash: 4f1cf3286e7b54dc90925bf2f1ab9fe8532022e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805973"
---
# <a name="pagesx-cell-print-properties-section"></a><span data-ttu-id="76b08-103">[PagesX] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="76b08-103">PagesX Cell (Print Properties Section)</span></span>

<span data-ttu-id="76b08-104">図面ページに左右を揃えるプリンター ページの番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="76b08-104">Determines the number of printer pages on which to fit the drawing page horizontally.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="76b08-105">備考</span><span class="sxs-lookup"><span data-stu-id="76b08-105">Remarks</span></span>

<span data-ttu-id="76b08-106">この値は、[OnPage] セルが TRUE に設定されているときに限り使用されます。</span><span class="sxs-lookup"><span data-stu-id="76b08-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="76b08-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [pagesx] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="76b08-107">To get a reference to the PagesX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76b08-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="76b08-108">Cell name:</span></span>  <br/> | <span data-ttu-id="76b08-109">[Pagesx]</span><span class="sxs-lookup"><span data-stu-id="76b08-109">PagesX</span></span>  <br/> |
   
<span data-ttu-id="76b08-110">プログラムから、インデックスによって [pagesx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="76b08-110">To get a reference to the PagesX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76b08-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="76b08-111">Section index:</span></span>  <br/> |<span data-ttu-id="76b08-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="76b08-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="76b08-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="76b08-113">Row index:</span></span>  <br/> |<span data-ttu-id="76b08-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="76b08-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="76b08-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="76b08-115">Cell index:</span></span>  <br/> |<span data-ttu-id="76b08-116">**visPrintPropertiesPagesX**</span><span class="sxs-lookup"><span data-stu-id="76b08-116">**visPrintPropertiesPagesX**</span></span> <br/> |
   

