---
title: '[SketchEnabled] セルl ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0baef353-41a1-4071-b5b4-ae342086fe34
description: 図形の上またはブール値としてではなく、スケッチ効果が表示されるかどうかを決定します。
ms.openlocfilehash: 7428d54eccce1a62d95a78dbc5fc6770fa5f1a77
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806506"
---
# <a name="sketchenabled-cell-additional-effect-properties-section"></a><span data-ttu-id="f8470-103">[SketchEnabled] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="f8470-103">SketchEnabled Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="f8470-104">図形の上またはブール値としてではなく、スケッチ効果が表示されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f8470-104">Determines whether a sketch effect is displayed on the shape or not, as a Boolean.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f8470-105">注釈</span><span class="sxs-lookup"><span data-stu-id="f8470-105">Remarks</span></span>

<span data-ttu-id="f8470-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **SketchEnabled** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="f8470-106">To get a reference to the **SketchEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8470-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="f8470-107">Cell name:</span></span>  <br/> | <span data-ttu-id="f8470-108">SketchEnabled</span><span class="sxs-lookup"><span data-stu-id="f8470-108">SketchEnabled</span></span>  <br/> |
   
<span data-ttu-id="f8470-109">プログラムから、インデックスによって [ **SketchEnabled** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f8470-109">To get a reference to the **SketchEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8470-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f8470-110">Section index:</span></span>  <br/> |<span data-ttu-id="f8470-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f8470-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f8470-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f8470-112">Row index:</span></span>  <br/> |<span data-ttu-id="f8470-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="f8470-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="f8470-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f8470-114">Cell index:</span></span>  <br/> |<span data-ttu-id="f8470-115">**visSketchEnabled**</span><span class="sxs-lookup"><span data-stu-id="f8470-115">**visSketchEnabled**</span></span> <br/> |
   

