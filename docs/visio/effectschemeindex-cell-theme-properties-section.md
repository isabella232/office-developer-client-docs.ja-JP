---
title: '[EffectSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 366ade40-e89f-49b6-b4be-4e4967dbacbf
description: 図形に適用されるテーマの効果設定を整数で指定します。
ms.openlocfilehash: 0d8ed18ca960868b1cd27abe517bfea99e1f2318
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321449"
---
# <a name="effectschemeindex-cell-theme-properties-section"></a><span data-ttu-id="80f69-103">[EffectSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="80f69-103">EffectSchemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="80f69-104">図形に適用されるテーマの効果設定を整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="80f69-104">Determines the effect scheme of the theme applied to a shape, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80f69-105">解説</span><span class="sxs-lookup"><span data-stu-id="80f69-105">Remarks</span></span>

<span data-ttu-id="80f69-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[effectschemeindex]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="80f69-106">To get a reference to the **EffectSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80f69-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="80f69-107">Cell name:</span></span>  <br/> | <span data-ttu-id="80f69-108">[effectschemeindex]</span><span class="sxs-lookup"><span data-stu-id="80f69-108">EffectSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="80f69-109">プログラムから、インデックスによって [ **[effectschemeindex]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="80f69-109">To get a reference to the **EffectSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80f69-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="80f69-110">Section index:</span></span>  <br/> |<span data-ttu-id="80f69-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="80f69-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="80f69-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="80f69-112">Row index:</span></span>  <br/> |<span data-ttu-id="80f69-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="80f69-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="80f69-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="80f69-114">Cell index:</span></span>  <br/> |<span data-ttu-id="80f69-115">\* \* visEffectSchemeIndex \* \*</span><span class="sxs-lookup"><span data-stu-id="80f69-115">\*\*visEffectSchemeIndex \*\*</span></span> <br/> |
   

