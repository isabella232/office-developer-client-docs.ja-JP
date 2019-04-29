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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407250"
---
# <a name="quickstylefontmatrix-cell-quick-style-section"></a><span data-ttu-id="21e43-103">[QuickStyleFontMatrix] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="21e43-103">QuickStyleFontMatrix Cell (Quick Style Section)</span></span>

<span data-ttu-id="21e43-104">各クイックスタイルのフォントのスタイルを、1 ~ 6 の整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="21e43-104">Determines the style of the font for each Quick Style, as an integer from 1 to 6.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21e43-105">注釈</span><span class="sxs-lookup"><span data-stu-id="21e43-105">Remarks</span></span>

<span data-ttu-id="21e43-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [**クイックスタイルのフォントマトリックス**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="21e43-106">To get a reference to the **QuickStyleFontMatrix** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="21e43-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="21e43-107">Cell name:</span></span>  <br/> | <span data-ttu-id="21e43-108">[quickstylefontmatrix]</span><span class="sxs-lookup"><span data-stu-id="21e43-108">QuickStyleFontMatrix</span></span>  <br/> |
   
<span data-ttu-id="21e43-109">プログラムから、インデックスによって [**クイックスタイルのフォントマトリックス**] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="21e43-109">To get a reference to the **QuickStyleFontMatrix** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="21e43-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="21e43-110">Section index:</span></span>  <br/> |<span data-ttu-id="21e43-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="21e43-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="21e43-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="21e43-112">Row index:</span></span>  <br/> |<span data-ttu-id="21e43-113">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="21e43-113">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="21e43-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="21e43-114">Cell index:</span></span>  <br/> |<span data-ttu-id="21e43-115">**visQuickStyleFontMatrix**</span><span class="sxs-lookup"><span data-stu-id="21e43-115">**visQuickStyleFontMatrix**</span></span> <br/> |
   

