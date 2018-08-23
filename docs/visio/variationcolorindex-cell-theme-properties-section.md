---
title: '[VariationColorIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea95a90c-4729-4689-a6f4-31dfccf37b9b
description: 整数値としてページで、アクティブなテーマのバリエーションの色のインデックスを決定します。
ms.openlocfilehash: b61317bc9048a6263e217e3eb29dc4dedcd911d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806753"
---
# <a name="variationcolorindex-cell-theme-properties-section"></a><span data-ttu-id="0cf15-103">[VariationColorIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="0cf15-103">VariationColorIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="0cf15-104">整数値としてページで、アクティブなテーマのバリエーションの色のインデックスを決定します。</span><span class="sxs-lookup"><span data-stu-id="0cf15-104">Determines the color index of the active theme variation on the page, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0cf15-105">注釈</span><span class="sxs-lookup"><span data-stu-id="0cf15-105">Remarks</span></span>

<span data-ttu-id="0cf15-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **VariationColorIndex** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="0cf15-106">To get a reference to the **VariationColorIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cf15-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="0cf15-107">Cell name:</span></span>  <br/> | <span data-ttu-id="0cf15-108">VariationColorIndex</span><span class="sxs-lookup"><span data-stu-id="0cf15-108">VariationColorIndex</span></span>  <br/> |
   
<span data-ttu-id="0cf15-109">プログラムから、インデックスによって [ **VariationColorIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="0cf15-109">To get a reference to the **VariationColorIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cf15-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0cf15-110">Section index:</span></span>  <br/> |<span data-ttu-id="0cf15-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0cf15-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0cf15-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0cf15-112">Row index:</span></span>  <br/> |<span data-ttu-id="0cf15-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="0cf15-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="0cf15-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0cf15-114">Cell index:</span></span>  <br/> |<span data-ttu-id="0cf15-115">**visVariationColorIndex**</span><span class="sxs-lookup"><span data-stu-id="0cf15-115">**visVariationColorIndex**</span></span> <br/> |
   

