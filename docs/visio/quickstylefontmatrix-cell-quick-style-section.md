---
title: '[QuickStyleFontMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 304ee083-e9c8-45df-b411-ba5e7db4c086
description: 各クイックスタイルのフォントのスタイルを、1 ~ 6 の整数で指定します。
ms.openlocfilehash: 0708a243b001c7b4e03158b5a332a3166727cabc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360075"
---
# <a name="quickstylefontmatrix-cell-quick-style-section"></a><span data-ttu-id="8986c-103">[QuickStyleFontMatrix] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="8986c-103">QuickStyleFontMatrix Cell (Quick Style Section)</span></span>

<span data-ttu-id="8986c-104">各クイックスタイルのフォントのスタイルを、1 ~ 6 の整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="8986c-104">Determines the style of the font for each Quick Style, as an integer from 1 to 6.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8986c-105">解説</span><span class="sxs-lookup"><span data-stu-id="8986c-105">Remarks</span></span>

<span data-ttu-id="8986c-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [**クイックスタイルのフォントマトリックス**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8986c-106">To get a reference to the **QuickStyleFontMatrix** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8986c-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="8986c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="8986c-108">[quickstylefontmatrix]</span><span class="sxs-lookup"><span data-stu-id="8986c-108">QuickStyleFontMatrix</span></span>  <br/> |
   
<span data-ttu-id="8986c-109">プログラムから、インデックスによって [**クイックスタイルのフォントマトリックス**] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8986c-109">To get a reference to the **QuickStyleFontMatrix** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8986c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8986c-110">Section index:</span></span>  <br/> |<span data-ttu-id="8986c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8986c-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8986c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8986c-112">Row index:</span></span>  <br/> |<span data-ttu-id="8986c-113">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="8986c-113">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="8986c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8986c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="8986c-115">**visQuickStyleFontMatrix**</span><span class="sxs-lookup"><span data-stu-id="8986c-115">**visQuickStyleFontMatrix**</span></span> <br/> |
   

