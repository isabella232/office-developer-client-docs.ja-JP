---
title: '[ThemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: 整数として、ドキュメントに適用される組み込みの Microsoft Visio のテーマの列挙体を格納します。 ドキュメントの新しいテーマを選択すると、組み込みのテーマのインデックスを使用してドキュメントとすべてのページと図形が含まれているの ThemeIndex のセルが更新されます。
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806636"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="c2251-104">[ThemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="c2251-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="c2251-105">整数として、ドキュメントに適用される組み込みの Microsoft Visio のテーマの列挙体を格納します。</span><span class="sxs-lookup"><span data-stu-id="c2251-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="c2251-106">ドキュメント、ドキュメントの**ThemeIndex**のセルに新しいテーマを選択したし、組み込みのテーマのインデックスを持つすべてのページとそれに含まれる図形が更新されます。</span><span class="sxs-lookup"><span data-stu-id="c2251-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c2251-107">備考</span><span class="sxs-lookup"><span data-stu-id="c2251-107">Remarks</span></span>

<span data-ttu-id="c2251-108">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ThemeIndex** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="c2251-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2251-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="c2251-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c2251-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="c2251-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="c2251-111">プログラムから、インデックスによって [ **ThemeIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c2251-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2251-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c2251-112">Section index:</span></span>  <br/> |<span data-ttu-id="c2251-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c2251-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c2251-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c2251-114">Row index:</span></span>  <br/> |<span data-ttu-id="c2251-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="c2251-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="c2251-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c2251-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c2251-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="c2251-117">**visThemeIndex**</span></span> <br/> |
   

