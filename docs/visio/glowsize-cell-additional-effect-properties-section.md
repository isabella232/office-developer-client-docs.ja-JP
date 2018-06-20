---
title: '[GlowSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ddc7a08-25b8-4903-b0dd-be72d1fa8075
description: ポイントで図形の外部の光彩のサイズを決定します。
ms.openlocfilehash: 71548843fd1d0e32f7c6e3949f1ae56dddb076fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805485"
---
# <a name="glowsize-cell-additional-effect-properties-section"></a><span data-ttu-id="3787b-103">[GlowSize] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="3787b-103">GlowSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="3787b-104">ポイントで図形の外部の光彩のサイズを決定します。</span><span class="sxs-lookup"><span data-stu-id="3787b-104">Determines the size of the external glow of a shape in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3787b-105">備考</span><span class="sxs-lookup"><span data-stu-id="3787b-105">Remarks</span></span>

<span data-ttu-id="3787b-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **GlowSize** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="3787b-106">To get a reference to the **GlowSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3787b-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="3787b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="3787b-108">GlowSize</span><span class="sxs-lookup"><span data-stu-id="3787b-108">GlowSize</span></span>  <br/> |
   
<span data-ttu-id="3787b-109">プログラムから、インデックスによって [ **GlowSize** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3787b-109">To get a reference to the **GlowSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3787b-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3787b-110">Section index:</span></span>  <br/> |<span data-ttu-id="3787b-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3787b-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3787b-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3787b-112">Row index:</span></span>  <br/> |<span data-ttu-id="3787b-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="3787b-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="3787b-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3787b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="3787b-115">**visGlowSize**</span><span class="sxs-lookup"><span data-stu-id="3787b-115">**visGlowSize**</span></span> <br/> |
   

