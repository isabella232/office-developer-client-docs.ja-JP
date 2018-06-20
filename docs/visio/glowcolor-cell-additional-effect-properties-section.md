---
title: '[GlowColor] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 640d18c0-5b6a-4a2f-9c81-f74de5ba9eb1
description: 図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。
ms.openlocfilehash: 167b08815f345903aed7ff1e92dd750461839dcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805468"
---
# <a name="glowcolor-cell-additional-effect-properties-section"></a><span data-ttu-id="4a64f-103">[GlowColor] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="4a64f-103">GlowColor Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="4a64f-104">図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。</span><span class="sxs-lookup"><span data-stu-id="4a64f-104">Determines the color used for the stroke of the external glow applied to a shape, as an RGB or theme value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a64f-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="4a64f-105">Remarks</span></span>

<span data-ttu-id="4a64f-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **GlowColor** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4a64f-106">To get a reference to the **GlowColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4a64f-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="4a64f-107">Cell name:</span></span>  <br/> | <span data-ttu-id="4a64f-108">GlowColor</span><span class="sxs-lookup"><span data-stu-id="4a64f-108">GlowColor</span></span>  <br/> |
   
<span data-ttu-id="4a64f-109">プログラムから、インデックスによって [ **GlowColor** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4a64f-109">To get a reference to the **GlowColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4a64f-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4a64f-110">Section index:</span></span>  <br/> |<span data-ttu-id="4a64f-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4a64f-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4a64f-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4a64f-112">Row index:</span></span>  <br/> |<span data-ttu-id="4a64f-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="4a64f-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="4a64f-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4a64f-114">Cell index:</span></span>  <br/> |<span data-ttu-id="4a64f-115">**visGlowColor**</span><span class="sxs-lookup"><span data-stu-id="4a64f-115">**visGlowColor**</span></span> <br/> |
   

