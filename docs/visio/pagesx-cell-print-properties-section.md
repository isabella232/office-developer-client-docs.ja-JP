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
ms.openlocfilehash: e912aef2277f5a7d2af5352897654ee986836c48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438695"
---
# <a name="pagesx-cell-print-properties-section"></a><span data-ttu-id="3d78c-103">[PagesX] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="3d78c-103">PagesX Cell (Print Properties Section)</span></span>

<span data-ttu-id="3d78c-104">図面ページに左右を揃えるプリンター ページの番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d78c-104">Determines the number of printer pages on which to fit the drawing page horizontally.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3d78c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="3d78c-105">Remarks</span></span>

<span data-ttu-id="3d78c-106">この値は、[OnPage] セルが TRUE に設定されているときに限り使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d78c-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="3d78c-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PagesX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d78c-107">To get a reference to the PagesX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d78c-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="3d78c-108">Cell name:</span></span>  <br/> | <span data-ttu-id="3d78c-109">[pagesx]</span><span class="sxs-lookup"><span data-stu-id="3d78c-109">PagesX</span></span>  <br/> |
   
<span data-ttu-id="3d78c-110">プログラムから、インデックスによって [PagesX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d78c-110">To get a reference to the PagesX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d78c-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3d78c-111">Section index:</span></span>  <br/> |<span data-ttu-id="3d78c-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3d78c-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3d78c-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3d78c-113">Row index:</span></span>  <br/> |<span data-ttu-id="3d78c-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="3d78c-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="3d78c-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3d78c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="3d78c-116">**visPrintPropertiesPagesX**</span><span class="sxs-lookup"><span data-stu-id="3d78c-116">**visPrintPropertiesPagesX**</span></span> <br/> |
   

