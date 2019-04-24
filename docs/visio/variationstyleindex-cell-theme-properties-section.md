---
title: '[VariationStyleIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 932195d5-2cb7-49f7-bc64-4ce00bf780b2
description: ページ上のアクティブなテーマのバリエーションのスタイルインデックスを整数で指定します。
ms.openlocfilehash: 57d4b2493b7278064daf7b0cb986e58ebacf4be2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355889"
---
# <a name="variationstyleindex-cell-theme-properties-section"></a><span data-ttu-id="28ecd-103">[VariationStyleIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="28ecd-103">VariationStyleIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="28ecd-104">ページ上のアクティブなテーマのバリエーションのスタイルインデックスを整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="28ecd-104">Determines the style index of the active theme variation on the page, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28ecd-105">解説</span><span class="sxs-lookup"><span data-stu-id="28ecd-105">Remarks</span></span>

<span data-ttu-id="28ecd-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [バリエーション] [**インデックス**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="28ecd-106">To get a reference to the **VariationStyleIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28ecd-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="28ecd-107">Cell name:</span></span>  <br/> | <span data-ttu-id="28ecd-108">[variationstyleindex]</span><span class="sxs-lookup"><span data-stu-id="28ecd-108">VariationStyleIndex</span></span>  <br/> |
   
<span data-ttu-id="28ecd-109">プログラムから、インデックスによって [バリエーション] [**インデックス**] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="28ecd-109">To get a reference to the **VariationStyleIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28ecd-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="28ecd-110">Section index:</span></span>  <br/> |<span data-ttu-id="28ecd-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="28ecd-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="28ecd-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="28ecd-112">Row index:</span></span>  <br/> |<span data-ttu-id="28ecd-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="28ecd-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="28ecd-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="28ecd-114">Cell index:</span></span>  <br/> |<span data-ttu-id="28ecd-115">**visVariationStyleIndex**</span><span class="sxs-lookup"><span data-stu-id="28ecd-115">**visVariationStyleIndex**</span></span> <br/> |
   

