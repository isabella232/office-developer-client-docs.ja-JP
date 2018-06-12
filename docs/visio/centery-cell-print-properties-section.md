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
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805020"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="a5b65-103">[CenterY] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="a5b65-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="a5b65-104">図面ページをプリンター ページの上下の中央に揃えるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a5b65-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="a5b65-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a5b65-105">**Value**</span></span>|<span data-ttu-id="a5b65-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a5b65-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a5b65-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a5b65-107">TRUE</span></span>  <br/> | <span data-ttu-id="a5b65-108">図面ページをプリンター ページの上下の中央に揃えます。</span><span class="sxs-lookup"><span data-stu-id="a5b65-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="a5b65-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a5b65-109">FALSE</span></span>  <br/> | <span data-ttu-id="a5b65-110">図面ページをプリンター ページの上下の中央に揃えません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="a5b65-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5b65-111">備考</span><span class="sxs-lookup"><span data-stu-id="a5b65-111">Remarks</span></span>

<span data-ttu-id="a5b65-p101">既定では、図面ページはプリンター ページの上と左に揃えられます。[CenterX] セルと [CenterY] セルを TRUE に設定すると、図面ページはプリンター ページの中央 (並べて表示する必要がある場合は複数ページの中央) に揃えられます。</span><span class="sxs-lookup"><span data-stu-id="a5b65-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="a5b65-114">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [centery] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a5b65-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a5b65-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="a5b65-115">Cell name:</span></span>  <br/> | <span data-ttu-id="a5b65-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="a5b65-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="a5b65-117">プログラムから、インデックスによって [centery] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a5b65-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a5b65-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a5b65-118">Section index:</span></span>  <br/> |<span data-ttu-id="a5b65-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a5b65-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a5b65-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a5b65-120">Row index:</span></span>  <br/> |<span data-ttu-id="a5b65-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="a5b65-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="a5b65-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a5b65-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a5b65-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="a5b65-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   
