---
title: '[QuickStyleFontMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 304ee083-e9c8-45df-b411-ba5e7db4c086
description: 1 ~ 6 の整数として各クイック スタイル、フォントのスタイルを決定します。
ms.openlocfilehash: 0c1c0d6279ba176dbb8db99c135108b1992b6202
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806135"
---
# <a name="quickstylefontmatrix-cell-quick-style-section"></a><span data-ttu-id="6c8f9-103">[QuickStyleFontMatrix] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="6c8f9-103">QuickStyleFontMatrix Cell (Quick Style Section)</span></span>

<span data-ttu-id="6c8f9-104">1 ~ 6 の整数として各クイック スタイル、フォントのスタイルを決定します。</span><span class="sxs-lookup"><span data-stu-id="6c8f9-104">Determines the style of the font for each Quick Style, as an integer from 1 to 6.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6c8f9-105">注釈</span><span class="sxs-lookup"><span data-stu-id="6c8f9-105">Remarks</span></span>

<span data-ttu-id="6c8f9-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **QuickStyleFontMatrix** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="6c8f9-106">To get a reference to the **QuickStyleFontMatrix** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c8f9-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="6c8f9-107">Cell name:</span></span>  <br/> | <span data-ttu-id="6c8f9-108">QuickStyleFontMatrix</span><span class="sxs-lookup"><span data-stu-id="6c8f9-108">QuickStyleFontMatrix</span></span>  <br/> |
   
<span data-ttu-id="6c8f9-109">プログラムから、インデックスによって [ **QuickStyleFontMatrix** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c8f9-109">To get a reference to the **QuickStyleFontMatrix** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c8f9-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6c8f9-110">Section index:</span></span>  <br/> |<span data-ttu-id="6c8f9-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6c8f9-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6c8f9-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6c8f9-112">Row index:</span></span>  <br/> |<span data-ttu-id="6c8f9-113">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="6c8f9-113">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="6c8f9-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6c8f9-114">Cell index:</span></span>  <br/> |<span data-ttu-id="6c8f9-115">**visQuickStyleFontMatrix**</span><span class="sxs-lookup"><span data-stu-id="6c8f9-115">**visQuickStyleFontMatrix**</span></span> <br/> |
   

