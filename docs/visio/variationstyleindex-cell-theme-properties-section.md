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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436602"
---
# <a name="variationstyleindex-cell-theme-properties-section"></a><span data-ttu-id="0911f-103">[VariationStyleIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="0911f-103">VariationStyleIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="0911f-104">ページ上のアクティブなテーマのバリエーションのスタイルインデックスを整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="0911f-104">Determines the style index of the active theme variation on the page, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0911f-105">注釈</span><span class="sxs-lookup"><span data-stu-id="0911f-105">Remarks</span></span>

<span data-ttu-id="0911f-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [バリエーション] [**インデックス**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0911f-106">To get a reference to the **VariationStyleIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0911f-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="0911f-107">Cell name:</span></span>  <br/> | <span data-ttu-id="0911f-108">[variationstyleindex]</span><span class="sxs-lookup"><span data-stu-id="0911f-108">VariationStyleIndex</span></span>  <br/> |
   
<span data-ttu-id="0911f-109">プログラムから、インデックスによって [バリエーション] [**インデックス**] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0911f-109">To get a reference to the **VariationStyleIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0911f-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0911f-110">Section index:</span></span>  <br/> |<span data-ttu-id="0911f-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0911f-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0911f-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0911f-112">Row index:</span></span>  <br/> |<span data-ttu-id="0911f-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="0911f-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="0911f-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0911f-114">Cell index:</span></span>  <br/> |<span data-ttu-id="0911f-115">**visVariationStyleIndex**</span><span class="sxs-lookup"><span data-stu-id="0911f-115">**visVariationStyleIndex**</span></span> <br/> |
   

