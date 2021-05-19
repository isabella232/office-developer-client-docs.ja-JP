---
title: '[QuickStyleEffectsMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0332bd3d-626a-4a46-8b69-e887e576ab86
description: アクティブなテーマから図形を継承するクイック スタイル効果を、0 から 6 の整数で決定します。
ms.openlocfilehash: 69541bd7371e8a02838a7ca075d136d8f49c316c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420130"
---
# <a name="quickstyleeffectsmatrix-cell-quick-style-section"></a><span data-ttu-id="c550a-103">[QuickStyleEffectsMatrix] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="c550a-103">QuickStyleEffectsMatrix Cell (Quick Style Section)</span></span>

<span data-ttu-id="c550a-104">アクティブなテーマから図形を継承するクイック スタイル効果を、0 から 6 の整数で決定します。</span><span class="sxs-lookup"><span data-stu-id="c550a-104">Determines the Quick Style effects that the shape inherits from the active theme, as an integer from 0-6.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c550a-105">注釈</span><span class="sxs-lookup"><span data-stu-id="c550a-105">Remarks</span></span>

<span data-ttu-id="c550a-106">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleEffectsMatrix** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c550a-106">To get a reference to the **QuickStyleEffectsMatrix** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c550a-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="c550a-107">Cell name:</span></span>  <br/> | <span data-ttu-id="c550a-108">QuickStyleEffectsMatrix</span><span class="sxs-lookup"><span data-stu-id="c550a-108">QuickStyleEffectsMatrix</span></span>  <br/> |
   
<span data-ttu-id="c550a-109">プログラムから、インデックスによって [**QuickStyleEffectsMatrix**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c550a-109">To get a reference to the **QuickStyleEffectsMatrix** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c550a-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c550a-110">Section index:</span></span>  <br/> |<span data-ttu-id="c550a-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c550a-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c550a-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c550a-112">Row index:</span></span>  <br/> |<span data-ttu-id="c550a-113">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="c550a-113">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="c550a-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c550a-114">Cell index:</span></span>  <br/> |<span data-ttu-id="c550a-115">**visQuickStyleEffectsMatrix**</span><span class="sxs-lookup"><span data-stu-id="c550a-115">**visQuickStyleEffectsMatrix**</span></span> <br/> |
   

