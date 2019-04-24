---
title: '[CenterY] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: 図面ページをプリンター ページの上下の中央に揃えるかどうかを指定します。
ms.openlocfilehash: 858bf41c74fdcbd82d271a379df7c5816a7796fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341917"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="a492e-103">[CenterY] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="a492e-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="a492e-104">図面ページをプリンター ページの上下の中央に揃えるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a492e-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="a492e-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a492e-105">**Value**</span></span>|<span data-ttu-id="a492e-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a492e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a492e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a492e-107">TRUE</span></span>  <br/> | <span data-ttu-id="a492e-108">図面ページをプリンター ページの上下の中央に揃えます。</span><span class="sxs-lookup"><span data-stu-id="a492e-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="a492e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a492e-109">FALSE</span></span>  <br/> | <span data-ttu-id="a492e-110">図面ページをプリンター ページの上下の中央に揃えません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="a492e-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a492e-111">解説</span><span class="sxs-lookup"><span data-stu-id="a492e-111">Remarks</span></span>

<span data-ttu-id="a492e-p101">既定では、図面ページはプリンター ページの上と左に揃えられます。[CenterX] セルと [CenterY] セルを TRUE に設定すると、図面ページはプリンター ページの中央 (並べて表示する必要がある場合は複数ページの中央) に揃えられます。</span><span class="sxs-lookup"><span data-stu-id="a492e-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="a492e-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [CenterY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a492e-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a492e-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="a492e-115">Cell name:</span></span>  <br/> | <span data-ttu-id="a492e-116">[centery]</span><span class="sxs-lookup"><span data-stu-id="a492e-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="a492e-117">プログラムから、インデックスによって [CenterY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a492e-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a492e-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a492e-118">Section index:</span></span>  <br/> |<span data-ttu-id="a492e-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a492e-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a492e-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a492e-120">Row index:</span></span>  <br/> |<span data-ttu-id="a492e-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="a492e-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="a492e-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a492e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a492e-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="a492e-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

