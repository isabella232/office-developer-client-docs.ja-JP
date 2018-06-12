---
title: '[CenterX] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: 図面ページをプリンター ページの左右の中央に揃えるかどうかを指定します。
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805001"
---
# <a name="centerx-cell-print-properties-section"></a><span data-ttu-id="65fc6-103">[CenterX] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="65fc6-103">CenterX Cell (Print Properties Section)</span></span>

<span data-ttu-id="65fc6-104">図面ページをプリンター ページの左右の中央に揃えるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="65fc6-104">Determines whether the drawing page is centered horizontally on the printer page.</span></span> 
  
|<span data-ttu-id="65fc6-105">**値**</span><span class="sxs-lookup"><span data-stu-id="65fc6-105">**Value**</span></span>|<span data-ttu-id="65fc6-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="65fc6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="65fc6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="65fc6-107">TRUE</span></span>  <br/> | <span data-ttu-id="65fc6-108">図面ページをプリンター ページの左右の中央に揃えます。</span><span class="sxs-lookup"><span data-stu-id="65fc6-108">Center the drawing page horizontally on the printer page.</span></span>  <br/> |
| <span data-ttu-id="65fc6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="65fc6-109">FALSE</span></span>  <br/> | <span data-ttu-id="65fc6-110">図面ページをプリンター ページの左右の中央に揃えません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="65fc6-110">Do not center the drawing page horizontally on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65fc6-111">備考</span><span class="sxs-lookup"><span data-stu-id="65fc6-111">Remarks</span></span>

<span data-ttu-id="65fc6-p101">既定では、図面ページはプリンター ページの上と左に揃えられます。[CenterX] セルと [CenterY] セルを TRUE に設定すると、図面ページはプリンター ページの中央 (並べて表示する必要がある場合は複数ページの中央) に揃えられます。</span><span class="sxs-lookup"><span data-stu-id="65fc6-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="65fc6-114">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [centerx] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="65fc6-114">To get a reference to the CenterX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="65fc6-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="65fc6-115">Cell name:</span></span>  <br/> | <span data-ttu-id="65fc6-116">[Centerx]</span><span class="sxs-lookup"><span data-stu-id="65fc6-116">CenterX</span></span>  <br/> |
   
<span data-ttu-id="65fc6-117">プログラムから、インデックスによって [centerx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="65fc6-117">To get a reference to the CenterX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="65fc6-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="65fc6-118">Section index:</span></span>  <br/> |<span data-ttu-id="65fc6-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="65fc6-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="65fc6-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="65fc6-120">Row index:</span></span>  <br/> |<span data-ttu-id="65fc6-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="65fc6-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="65fc6-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="65fc6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="65fc6-123">**visPrintPropertiesCenterX**</span><span class="sxs-lookup"><span data-stu-id="65fc6-123">**visPrintPropertiesCenterX**</span></span> <br/> |
   

