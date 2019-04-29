---
title: '[GlowColorTrans] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6cf67cb-f9e6-43a5-918a-f9151821ab4d
description: 図形の光彩のストロークに使用する色の透過性レベルをパーセンテージで指定します。
ms.openlocfilehash: 81b734de6212540e0f50df05aca11dc535fc49ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439752"
---
# <a name="glowcolortrans-cell-additional-effect-properties-section"></a><span data-ttu-id="3aaea-103">[GlowColorTrans] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="3aaea-103">GlowColorTrans Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="3aaea-104">図形の光彩のストロークに使用する色の透過性レベルをパーセンテージで指定します。</span><span class="sxs-lookup"><span data-stu-id="3aaea-104">Determines the transparency level for the color used for the stroke of the shape's glow, as a percentage.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3aaea-105">注釈</span><span class="sxs-lookup"><span data-stu-id="3aaea-105">Remarks</span></span>

<span data-ttu-id="3aaea-106">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**GlowColorTrans**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3aaea-106">To get a reference to the **GlowColorTrans** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3aaea-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="3aaea-107">Cell name:</span></span>  <br/> | <span data-ttu-id="3aaea-108">[glowcolortrans]</span><span class="sxs-lookup"><span data-stu-id="3aaea-108">GlowColorTrans</span></span>  <br/> |
   
<span data-ttu-id="3aaea-109">プログラムから、インデックスによって [**GlowColorTrans**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3aaea-109">To get a reference to the **GlowColorTrans** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3aaea-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3aaea-110">Section index:</span></span>  <br/> |<span data-ttu-id="3aaea-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3aaea-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3aaea-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3aaea-112">Row index:</span></span>  <br/> |<span data-ttu-id="3aaea-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="3aaea-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="3aaea-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3aaea-114">Cell index:</span></span>  <br/> |<span data-ttu-id="3aaea-115">**visGlowColorTrans**</span><span class="sxs-lookup"><span data-stu-id="3aaea-115">**visGlowColorTrans**</span></span> <br/> |
   

