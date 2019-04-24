---
title: '[VariationColorIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea95a90c-4729-4689-a6f4-31dfccf37b9b
description: ページ上のアクティブなテーマのバリエーションの色のインデックスを整数で指定します。
ms.openlocfilehash: 7582b779fb5be6bdf3528da137b1b08b8cd9c01a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355882"
---
# <a name="variationcolorindex-cell-theme-properties-section"></a><span data-ttu-id="28638-103">[VariationColorIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="28638-103">VariationColorIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="28638-104">ページ上のアクティブなテーマのバリエーションの色のインデックスを整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="28638-104">Determines the color index of the active theme variation on the page, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28638-105">解説</span><span class="sxs-lookup"><span data-stu-id="28638-105">Remarks</span></span>

<span data-ttu-id="28638-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[variationcolorindex]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="28638-106">To get a reference to the **VariationColorIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28638-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="28638-107">Cell name:</span></span>  <br/> | <span data-ttu-id="28638-108">[variationcolorindex]</span><span class="sxs-lookup"><span data-stu-id="28638-108">VariationColorIndex</span></span>  <br/> |
   
<span data-ttu-id="28638-109">プログラムから、インデックスによって [ **[variationcolorindex]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="28638-109">To get a reference to the **VariationColorIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28638-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="28638-110">Section index:</span></span>  <br/> |<span data-ttu-id="28638-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="28638-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="28638-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="28638-112">Row index:</span></span>  <br/> |<span data-ttu-id="28638-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="28638-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="28638-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="28638-114">Cell index:</span></span>  <br/> |<span data-ttu-id="28638-115">**visVariationColorIndex**</span><span class="sxs-lookup"><span data-stu-id="28638-115">**visVariationColorIndex**</span></span> <br/> |
   

