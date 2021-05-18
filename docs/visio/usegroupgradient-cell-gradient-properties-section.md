---
title: '[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: 図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。[UseGroupGradient] セルの値が影響するのは、図形の塗りつぶしのみです。
ms.openlocfilehash: a69b48095aec93705c686a5401051f1d1e368d18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411366"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a><span data-ttu-id="6aede-104">[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="6aede-104">UseGroupGradient Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="6aede-p102">図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。[**UseGroupGradient**] セルの値が影響するのは、図形の塗りつぶしのみです。</span><span class="sxs-lookup"><span data-stu-id="6aede-p102">Determines whether the shape takes on a gradient when the shape is grouped together with other shapes, as a Boolean. The value of **UseGroupGradient** cell affects the shape fill only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6aede-107">注釈</span><span class="sxs-lookup"><span data-stu-id="6aede-107">Remarks</span></span>

<span data-ttu-id="6aede-108">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**UseGroupGradient**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6aede-108">To get a reference to the **UseGroupGradient** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6aede-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="6aede-109">Cell name:</span></span>  <br/> | <span data-ttu-id="6aede-110">UseGroupGradient</span><span class="sxs-lookup"><span data-stu-id="6aede-110">UseGroupGradient</span></span>  <br/> |
   
<span data-ttu-id="6aede-111">プログラムから、インデックスによって [**UseGroupGradient**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6aede-111">To get a reference to the **UseGroupGradient** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6aede-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6aede-112">Section index:</span></span>  <br/> |<span data-ttu-id="6aede-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6aede-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6aede-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6aede-114">Row index:</span></span>  <br/> |<span data-ttu-id="6aede-115">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="6aede-115">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="6aede-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6aede-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6aede-117">\*\*visUseGroupGradient \*\*</span><span class="sxs-lookup"><span data-stu-id="6aede-117">\*\*visUseGroupGradient \*\*</span></span> <br/> |
   

