---
title: '[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb84f71e-59c4-43d4-a28b-c3d6f267d2ae
description: 図形の配色が後に続くテーマのインデックスを整数で指定します。
ms.openlocfilehash: d67363b48454a717914b8ff9e39952609d848118
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430764"
---
# <a name="colorschemeindex-cell-theme-properties-section"></a><span data-ttu-id="e39f4-103">[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="e39f4-103">ColorSchemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="e39f4-104">図形の配色が後に続くテーマのインデックスを整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="e39f4-104">Determines the index of the theme that the shape's color scheme takes after, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e39f4-105">注釈</span><span class="sxs-lookup"><span data-stu-id="e39f4-105">Remarks</span></span>

<span data-ttu-id="e39f4-106">別の数式 **、Cell** 要素の **N** 属性の値、または **CellsU** プロパティを使用するプログラムから、名前によって **ColorSchemeIndex** セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e39f4-106">To get a reference to the **ColorSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e39f4-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="e39f4-107">Cell name:</span></span>  <br/> | <span data-ttu-id="e39f4-108">ColorSchemeIndex</span><span class="sxs-lookup"><span data-stu-id="e39f4-108">ColorSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="e39f4-109">プログラムからインデックスによって **ColorSchemeIndex** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e39f4-109">To get a reference to the **ColorSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e39f4-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e39f4-110">Section index:</span></span>  <br/> |<span data-ttu-id="e39f4-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e39f4-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e39f4-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e39f4-112">Row index:</span></span>  <br/> |<span data-ttu-id="e39f4-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="e39f4-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="e39f4-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e39f4-114">Cell index:</span></span>  <br/> |<span data-ttu-id="e39f4-115">**visColorSchemeIndex**</span><span class="sxs-lookup"><span data-stu-id="e39f4-115">**visColorSchemeIndex**</span></span> <br/> |
   

