---
title: '[EffectSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 366ade40-e89f-49b6-b4be-4e4967dbacbf
description: 整数値で、図形に適用するテーマの効果設定を決定します。
ms.openlocfilehash: 369eb059633a7efc27ee670c400f383205bceea6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805297"
---
# <a name="effectschemeindex-cell-theme-properties-section"></a><span data-ttu-id="20925-103">[EffectSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="20925-103">EffectSchemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="20925-104">整数値で、図形に適用するテーマの効果設定を決定します。</span><span class="sxs-lookup"><span data-stu-id="20925-104">Determines the effect scheme of the theme applied to a shape, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20925-105">注釈</span><span class="sxs-lookup"><span data-stu-id="20925-105">Remarks</span></span>

<span data-ttu-id="20925-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **EffectSchemeIndex** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="20925-106">To get a reference to the **EffectSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20925-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="20925-107">Cell name:</span></span>  <br/> | <span data-ttu-id="20925-108">EffectSchemeIndex</span><span class="sxs-lookup"><span data-stu-id="20925-108">EffectSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="20925-109">プログラムから、インデックスによって [ **EffectSchemeIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="20925-109">To get a reference to the **EffectSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20925-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="20925-110">Section index:</span></span>  <br/> |<span data-ttu-id="20925-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20925-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20925-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="20925-112">Row index:</span></span>  <br/> |<span data-ttu-id="20925-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="20925-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="20925-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="20925-114">Cell index:</span></span>  <br/> |<span data-ttu-id="20925-115">* * visEffectSchemeIndex * *</span><span class="sxs-lookup"><span data-stu-id="20925-115">**visEffectSchemeIndex **</span></span> <br/> |
   

