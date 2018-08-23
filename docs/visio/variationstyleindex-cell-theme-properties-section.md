---
title: '[VariationStyleIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 932195d5-2cb7-49f7-bc64-4ce00bf780b2
description: 整数値としてページで、アクティブなテーマのバリエーションのスタイルのインデックスを決定します。
ms.openlocfilehash: fc29d95c6601303671e83e2c89f693447550c5f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806758"
---
# <a name="variationstyleindex-cell-theme-properties-section"></a><span data-ttu-id="30d05-103">[VariationStyleIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="30d05-103">VariationStyleIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="30d05-104">整数値としてページで、アクティブなテーマのバリエーションのスタイルのインデックスを決定します。</span><span class="sxs-lookup"><span data-stu-id="30d05-104">Determines the style index of the active theme variation on the page, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30d05-105">注釈</span><span class="sxs-lookup"><span data-stu-id="30d05-105">Remarks</span></span>

<span data-ttu-id="30d05-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **VariationStyleIndex** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="30d05-106">To get a reference to the **VariationStyleIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30d05-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="30d05-107">Cell name:</span></span>  <br/> | <span data-ttu-id="30d05-108">VariationStyleIndex</span><span class="sxs-lookup"><span data-stu-id="30d05-108">VariationStyleIndex</span></span>  <br/> |
   
<span data-ttu-id="30d05-109">プログラムから、インデックスによって [ **VariationStyleIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="30d05-109">To get a reference to the **VariationStyleIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30d05-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="30d05-110">Section index:</span></span>  <br/> |<span data-ttu-id="30d05-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="30d05-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="30d05-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="30d05-112">Row index:</span></span>  <br/> |<span data-ttu-id="30d05-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="30d05-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="30d05-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="30d05-114">Cell index:</span></span>  <br/> |<span data-ttu-id="30d05-115">**visVariationStyleIndex**</span><span class="sxs-lookup"><span data-stu-id="30d05-115">**visVariationStyleIndex**</span></span> <br/> |
   

