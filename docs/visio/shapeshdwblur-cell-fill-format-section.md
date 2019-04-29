---
title: '[ShapeShdwBlur] セル ([塗りつぶしの書式設定] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 90ace659-d979-43e1-ac64-25af3ec5d666
description: 図形の影のぼかしのサイズをポイント単位 (0.00 ~ 100.00) で指定します。
ms.openlocfilehash: ae559cbb183266dbba3ed0e98c98d24db71f3b58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424988"
---
# <a name="shapeshdwblur-cell-fill-format-section"></a><span data-ttu-id="8470c-103">[ShapeShdwBlur] セル ([塗りつぶしの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="8470c-103">ShapeShdwBlur Cell (Fill Format Section)</span></span>

<span data-ttu-id="8470c-104">図形の影のぼかしのサイズをポイント単位 (0.00 ~ 100.00) で指定します。</span><span class="sxs-lookup"><span data-stu-id="8470c-104">Determines the size of the blur for a shape's shadow, in points (0.00 to 100.00).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8470c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="8470c-105">Remarks</span></span>

<span data-ttu-id="8470c-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[shapeshdwblur]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8470c-106">To get a reference to the **ShapeShdwBlur** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8470c-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="8470c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="8470c-108">[shapeshdwblur]</span><span class="sxs-lookup"><span data-stu-id="8470c-108">ShapeShdwBlur</span></span>  <br/> |
   
<span data-ttu-id="8470c-109">プログラムから、インデックスによって [ **[shapeshdwblur]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8470c-109">To get a reference to the **ShapeShdwBlur** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8470c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8470c-110">Section index:</span></span>  <br/> |<span data-ttu-id="8470c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8470c-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8470c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8470c-112">Row index:</span></span>  <br/> |<span data-ttu-id="8470c-113">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="8470c-113">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="8470c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8470c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="8470c-115">**visFillShdwBlur**</span><span class="sxs-lookup"><span data-stu-id="8470c-115">**visFillShdwBlur**</span></span> <br/> |
   

