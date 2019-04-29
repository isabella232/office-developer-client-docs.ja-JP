---
title: '[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb84f71e-59c4-43d4-a28b-c3d6f267d2ae
description: 図形の配色が後にかかるテーマのインデックスを整数で指定します。
ms.openlocfilehash: d67363b48454a717914b8ff9e39952609d848118
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430764"
---
# <a name="colorschemeindex-cell-theme-properties-section"></a><span data-ttu-id="35701-103">[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="35701-103">ColorSchemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="35701-104">図形の配色が後にかかるテーマのインデックスを整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="35701-104">Determines the index of the theme that the shape's color scheme takes after, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35701-105">注釈</span><span class="sxs-lookup"><span data-stu-id="35701-105">Remarks</span></span>

<span data-ttu-id="35701-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[colorschemeindex]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="35701-106">To get a reference to the **ColorSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35701-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="35701-107">Cell name:</span></span>  <br/> | <span data-ttu-id="35701-108">[colorschemeindex]</span><span class="sxs-lookup"><span data-stu-id="35701-108">ColorSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="35701-109">プログラムから、インデックスによって [ **[colorschemeindex]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="35701-109">To get a reference to the **ColorSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35701-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="35701-110">Section index:</span></span>  <br/> |<span data-ttu-id="35701-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="35701-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="35701-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="35701-112">Row index:</span></span>  <br/> |<span data-ttu-id="35701-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="35701-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="35701-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="35701-114">Cell index:</span></span>  <br/> |<span data-ttu-id="35701-115">**visColorSchemeIndex**</span><span class="sxs-lookup"><span data-stu-id="35701-115">**visColorSchemeIndex**</span></span> <br/> |
   

