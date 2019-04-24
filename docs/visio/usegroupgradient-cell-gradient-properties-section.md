---
title: '[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: 図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。 [UseGroupGradient] セルの値が影響するのは、図形の塗りつぶしのみです。
ms.openlocfilehash: a69b48095aec93705c686a5401051f1d1e368d18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337157"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a><span data-ttu-id="1ff18-104">[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="1ff18-104">UseGroupGradient Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="1ff18-105">図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。</span><span class="sxs-lookup"><span data-stu-id="1ff18-105">Determines whether the shape takes on a gradient when the shape is grouped together with other shapes, as a Boolean.</span></span> <span data-ttu-id="1ff18-106">[**UseGroupGradient**] セルの値が影響するのは、図形の塗りつぶしのみです。</span><span class="sxs-lookup"><span data-stu-id="1ff18-106">The value of **UseGroupGradient** cell affects the shape fill only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1ff18-107">解説</span><span class="sxs-lookup"><span data-stu-id="1ff18-107">Remarks</span></span>

<span data-ttu-id="1ff18-108">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**UseGroupGradient**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ff18-108">To get a reference to the **UseGroupGradient** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ff18-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="1ff18-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1ff18-110">[usegroupgradient]</span><span class="sxs-lookup"><span data-stu-id="1ff18-110">UseGroupGradient</span></span>  <br/> |
   
<span data-ttu-id="1ff18-111">プログラムから、インデックスによって [**UseGroupGradient**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ff18-111">To get a reference to the **UseGroupGradient** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ff18-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1ff18-112">Section index:</span></span>  <br/> |<span data-ttu-id="1ff18-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1ff18-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1ff18-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1ff18-114">Row index:</span></span>  <br/> |<span data-ttu-id="1ff18-115">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="1ff18-115">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="1ff18-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1ff18-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1ff18-117">\* \* visUseGroupGradient \* \*</span><span class="sxs-lookup"><span data-stu-id="1ff18-117">\*\*visUseGroupGradient \*\*</span></span> <br/> |
   

