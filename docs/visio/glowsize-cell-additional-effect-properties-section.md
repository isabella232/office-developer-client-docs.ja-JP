---
title: '[GlowSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ddc7a08-25b8-4903-b0dd-be72d1fa8075
description: 図形の外側の光彩のサイズをポイント単位で指定します。
ms.openlocfilehash: 6d338ebe23b5c5422c7cdc5a72fccb18eefef87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359109"
---
# <a name="glowsize-cell-additional-effect-properties-section"></a><span data-ttu-id="648a6-103">[GlowSize] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="648a6-103">GlowSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="648a6-104">図形の外側の光彩のサイズをポイント単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="648a6-104">Determines the size of the external glow of a shape in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="648a6-105">解説</span><span class="sxs-lookup"><span data-stu-id="648a6-105">Remarks</span></span>

<span data-ttu-id="648a6-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[glowsize]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="648a6-106">To get a reference to the **GlowSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="648a6-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="648a6-107">Cell name:</span></span>  <br/> | <span data-ttu-id="648a6-108">[glowsize]</span><span class="sxs-lookup"><span data-stu-id="648a6-108">GlowSize</span></span>  <br/> |
   
<span data-ttu-id="648a6-109">プログラムから、インデックスによって [ **[glowsize]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="648a6-109">To get a reference to the **GlowSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="648a6-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="648a6-110">Section index:</span></span>  <br/> |<span data-ttu-id="648a6-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="648a6-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="648a6-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="648a6-112">Row index:</span></span>  <br/> |<span data-ttu-id="648a6-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="648a6-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="648a6-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="648a6-114">Cell index:</span></span>  <br/> |<span data-ttu-id="648a6-115">**visGlowSize**</span><span class="sxs-lookup"><span data-stu-id="648a6-115">**visGlowSize**</span></span> <br/> |
   

