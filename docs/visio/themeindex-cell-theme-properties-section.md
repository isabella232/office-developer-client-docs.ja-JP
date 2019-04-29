---
title: '[ThemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: ドキュメントに適用されている組み込みの Microsoft Visio テーマの列挙を整数として格納します。 新しいテーマをドキュメント用に選択した場合、ドキュメントの [ThemeIndex] セルとそこに格納されたすべてのページと図形が、組み込みテーマのインデックスを使用して更新されます。
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411912"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="b3f9a-104">[ThemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="b3f9a-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="b3f9a-105">ドキュメントに適用されている組み込みの Microsoft Visio テーマの列挙を整数として格納します。</span><span class="sxs-lookup"><span data-stu-id="b3f9a-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="b3f9a-106">新しいテーマをドキュメント用に選択した場合、ドキュメントの [**ThemeIndex**] セルとそこに格納されたすべてのページと図形が、組み込みテーマのインデックスを使用して更新されます。</span><span class="sxs-lookup"><span data-stu-id="b3f9a-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b3f9a-107">注釈</span><span class="sxs-lookup"><span data-stu-id="b3f9a-107">Remarks</span></span>

<span data-ttu-id="b3f9a-108">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ThemeIndex**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3f9a-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3f9a-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="b3f9a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b3f9a-110">[themeindex]</span><span class="sxs-lookup"><span data-stu-id="b3f9a-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="b3f9a-111">プログラムから、インデックスによって [**ThemeIndex**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b3f9a-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3f9a-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b3f9a-112">Section index:</span></span>  <br/> |<span data-ttu-id="b3f9a-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3f9a-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b3f9a-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b3f9a-114">Row index:</span></span>  <br/> |<span data-ttu-id="b3f9a-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="b3f9a-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="b3f9a-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b3f9a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b3f9a-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="b3f9a-117">**visThemeIndex**</span></span> <br/> |
   

