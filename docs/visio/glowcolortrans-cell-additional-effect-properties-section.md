---
title: '[GlowColorTrans] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6cf67cb-f9e6-43a5-918a-f9151821ab4d
description: パーセントでの図形の光彩、線の色の透過性レベルを決定します。
ms.openlocfilehash: b4826c4b398198c48f908324f56b7b9a3156d881
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805475"
---
# <a name="glowcolortrans-cell-additional-effect-properties-section"></a><span data-ttu-id="31000-103">[GlowColorTrans] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="31000-103">GlowColorTrans Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="31000-104">パーセントでの図形の光彩、線の色の透過性レベルを決定します。</span><span class="sxs-lookup"><span data-stu-id="31000-104">Determines the transparency level for the color used for the stroke of the shape's glow, as a percentage.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="31000-105">注釈</span><span class="sxs-lookup"><span data-stu-id="31000-105">Remarks</span></span>

<span data-ttu-id="31000-106">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**GlowColorTrans**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="31000-106">To get a reference to the **GlowColorTrans** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31000-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="31000-107">Cell name:</span></span>  <br/> | <span data-ttu-id="31000-108">GlowColorTrans</span><span class="sxs-lookup"><span data-stu-id="31000-108">GlowColorTrans</span></span>  <br/> |
   
<span data-ttu-id="31000-109">プログラムから、インデックスによって [**GlowColorTrans**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="31000-109">To get a reference to the **GlowColorTrans** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31000-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="31000-110">Section index:</span></span>  <br/> |<span data-ttu-id="31000-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="31000-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="31000-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="31000-112">Row index:</span></span>  <br/> |<span data-ttu-id="31000-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="31000-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="31000-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="31000-114">Cell index:</span></span>  <br/> |<span data-ttu-id="31000-115">**visGlowColorTrans**</span><span class="sxs-lookup"><span data-stu-id="31000-115">**visGlowColorTrans**</span></span> <br/> |
   

