---
title: '[GlowColor] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 640d18c0-5b6a-4a2f-9c81-f74de5ba9eb1
description: 図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。
ms.openlocfilehash: 726dbef7ae006af1a6ff9956d16eb73cfdd02974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422636"
---
# <a name="glowcolor-cell-additional-effect-properties-section"></a><span data-ttu-id="24a7c-103">[GlowColor] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="24a7c-103">GlowColor Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="24a7c-104">図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。</span><span class="sxs-lookup"><span data-stu-id="24a7c-104">Determines the color used for the stroke of the external glow applied to a shape, as an RGB or theme value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24a7c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="24a7c-105">Remarks</span></span>

<span data-ttu-id="24a7c-106">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**GlowColor**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="24a7c-106">To get a reference to the **GlowColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24a7c-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="24a7c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="24a7c-108">GlowColor</span><span class="sxs-lookup"><span data-stu-id="24a7c-108">GlowColor</span></span>  <br/> |
   
<span data-ttu-id="24a7c-109">プログラムから、インデックスによって [**GlowColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="24a7c-109">To get a reference to the **GlowColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24a7c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="24a7c-110">Section index:</span></span>  <br/> |<span data-ttu-id="24a7c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24a7c-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="24a7c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="24a7c-112">Row index:</span></span>  <br/> |<span data-ttu-id="24a7c-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="24a7c-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="24a7c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="24a7c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="24a7c-115">**visGlowColor**</span><span class="sxs-lookup"><span data-stu-id="24a7c-115">**visGlowColor**</span></span> <br/> |
   

