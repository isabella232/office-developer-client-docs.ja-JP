---
title: '[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb84f71e-59c4-43d4-a28b-c3d6f267d2ae
description: テーマを整数として後、は、図形の配色パターンのインデックスを決定します。
ms.openlocfilehash: 03f354890c8dbce74da6b1171b3b3aaf4bf73ad3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805040"
---
# <a name="colorschemeindex-cell-theme-properties-section"></a><span data-ttu-id="5ed83-103">[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="5ed83-103">ColorSchemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="5ed83-104">テーマを整数として後、は、図形の配色パターンのインデックスを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ed83-104">Determines the index of the theme that the shape's color scheme takes after, as an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ed83-105">備考</span><span class="sxs-lookup"><span data-stu-id="5ed83-105">Remarks</span></span>

<span data-ttu-id="5ed83-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ColorSchemeIndex** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="5ed83-106">To get a reference to the **ColorSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ed83-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="5ed83-107">Cell name:</span></span>  <br/> | <span data-ttu-id="5ed83-108">ColorSchemeIndex</span><span class="sxs-lookup"><span data-stu-id="5ed83-108">ColorSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="5ed83-109">プログラムから、インデックスによって [ **ColorSchemeIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5ed83-109">To get a reference to the **ColorSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ed83-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5ed83-110">Section index:</span></span>  <br/> |<span data-ttu-id="5ed83-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5ed83-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5ed83-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5ed83-112">Row index:</span></span>  <br/> |<span data-ttu-id="5ed83-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="5ed83-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="5ed83-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5ed83-114">Cell index:</span></span>  <br/> |<span data-ttu-id="5ed83-115">**visColorSchemeIndex**</span><span class="sxs-lookup"><span data-stu-id="5ed83-115">**visColorSchemeIndex**</span></span> <br/> |
   

