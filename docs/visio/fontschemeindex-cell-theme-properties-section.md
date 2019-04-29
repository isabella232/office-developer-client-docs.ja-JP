---
title: '[FontSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b832d75b-dac2-495f-b86e-d7fc5a484cab
description: 図形に適用するテーマのフォントパターンを整数で指定します。
ms.openlocfilehash: 3a527b93b95f86dc1b9b92c931f3877ef28523ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420501"
---
# <a name="fontschemeindex-cell-theme-properties-section"></a><span data-ttu-id="fda1a-103">[FontSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="fda1a-103">FontSchemeIndex Cell (Theme Properties Section</span></span>

<span data-ttu-id="fda1a-104">図形に適用するテーマのフォントパターンを整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="fda1a-104">Determines the font scheme of a theme that is applied to the shape, as an integer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fda1a-105">注釈</span><span class="sxs-lookup"><span data-stu-id="fda1a-105">Remarks</span></span>

<span data-ttu-id="fda1a-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[fontschemeindex]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fda1a-106">To get a reference to the **FontSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fda1a-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="fda1a-107">Cell name:</span></span>  <br/> | <span data-ttu-id="fda1a-108">[fontschemeindex]</span><span class="sxs-lookup"><span data-stu-id="fda1a-108">FontSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="fda1a-109">プログラムから、インデックスによって [ **[fontschemeindex]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fda1a-109">To get a reference to the **FontSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fda1a-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fda1a-110">Section index:</span></span>  <br/> |<span data-ttu-id="fda1a-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fda1a-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fda1a-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fda1a-112">Row index:</span></span>  <br/> |<span data-ttu-id="fda1a-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="fda1a-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="fda1a-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fda1a-114">Cell index:</span></span>  <br/> |<span data-ttu-id="fda1a-115">**visFontSchemeIndex**</span><span class="sxs-lookup"><span data-stu-id="fda1a-115">**visFontSchemeIndex**</span></span> <br/> |
   

