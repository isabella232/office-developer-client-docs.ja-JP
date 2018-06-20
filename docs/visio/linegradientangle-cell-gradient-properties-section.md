---
title: '[LineGradientAngle] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b533ea0-5d2e-44fc-a691-8fa2f310ff9f
description: 359.9 に 0 からの線形のグラデーションの線のグラデーションの角度を決定します。
ms.openlocfilehash: 8db4c7ba4bd62bfae4ec3444aef832450363763b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805691"
---
# <a name="linegradientangle-cell-gradient-properties-section"></a><span data-ttu-id="878c3-103">[LineGradientAngle] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="878c3-103">LineGradientAngle Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="878c3-104">359.9 に 0 からの線形のグラデーションの線のグラデーションの角度を決定します。</span><span class="sxs-lookup"><span data-stu-id="878c3-104">Determines the angle of the line gradient for a linear gradient, from 0 to 359.9 degrees.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="878c3-105">備考</span><span class="sxs-lookup"><span data-stu-id="878c3-105">Remarks</span></span>

<span data-ttu-id="878c3-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LineGradientAngle** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="878c3-106">To get a reference to the **LineGradientAngle** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="878c3-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="878c3-107">Cell name:</span></span>  <br/> | <span data-ttu-id="878c3-108">LineGradientAngle</span><span class="sxs-lookup"><span data-stu-id="878c3-108">LineGradientAngle</span></span>  <br/> |
   
<span data-ttu-id="878c3-109">プログラムから、インデックスによって [ **LineGradientAngle** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="878c3-109">To get a reference to the **LineGradientAngle** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="878c3-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="878c3-110">Section index:</span></span>  <br/> |<span data-ttu-id="878c3-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="878c3-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="878c3-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="878c3-112">Row index:</span></span>  <br/> |<span data-ttu-id="878c3-113">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="878c3-113">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="878c3-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="878c3-114">Cell index:</span></span>  <br/> |<span data-ttu-id="878c3-115">**visLineGradientAngle**</span><span class="sxs-lookup"><span data-stu-id="878c3-115">**visLineGradientAngle**</span></span> <br/> |
   

