---
title: '[PagesY] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: 図面ページに上下を揃えるプリンター ページの番号を指定します。
ms.openlocfilehash: 1663fac8efdf06599d1e3c00d5eb0d00ec52e476
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805966"
---
# <a name="pagesy-cell-print-properties-section"></a><span data-ttu-id="847c2-103">[PagesY] セル ([印刷のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="847c2-103">PagesY Cell (Print Properties Section)</span></span>

<span data-ttu-id="847c2-104">図面ページに上下を揃えるプリンター ページの番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="847c2-104">Determines the number of printer pages on which to fit the drawing page vertically.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="847c2-105">備考</span><span class="sxs-lookup"><span data-stu-id="847c2-105">Remarks</span></span>

<span data-ttu-id="847c2-106">この値は、[OnPage] セルが TRUE に設定されているときに限り使用されます。</span><span class="sxs-lookup"><span data-stu-id="847c2-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="847c2-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PagesY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="847c2-107">To get a reference to the PagesY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="847c2-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="847c2-108">Cell name:</span></span>  <br/> | <span data-ttu-id="847c2-109">[Pagesy]</span><span class="sxs-lookup"><span data-stu-id="847c2-109">PagesY</span></span>  <br/> |
   
<span data-ttu-id="847c2-110">プログラムから、インデックスによって [PagesY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="847c2-110">To get a reference to the PagesY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="847c2-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="847c2-111">Section index:</span></span>  <br/> |<span data-ttu-id="847c2-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="847c2-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="847c2-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="847c2-113">Row index:</span></span>  <br/> |<span data-ttu-id="847c2-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="847c2-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="847c2-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="847c2-115">Cell index:</span></span>  <br/> |<span data-ttu-id="847c2-116">**visPrintPropertiesPagesY**</span><span class="sxs-lookup"><span data-stu-id="847c2-116">**visPrintPropertiesPagesY**</span></span> <br/> |
   

