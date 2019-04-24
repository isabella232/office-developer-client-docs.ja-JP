---
title: '[Width] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 選択した図形の幅を図面の単位で表した値が表示されます。 1-D 図形の幅を決定する既定の数式は次のとおりです。
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351220"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="bd32f-104">[Width] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="bd32f-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="bd32f-105">選択した図形の幅を図面の単位で表した値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bd32f-105">Contains the width of the selected shape in drawing units.</span></span> <span data-ttu-id="bd32f-106">1-D 図形の幅を決定する既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bd32f-106">The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="bd32f-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="bd32f-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd32f-108">解説</span><span class="sxs-lookup"><span data-stu-id="bd32f-108">Remarks</span></span>

<span data-ttu-id="bd32f-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Width] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bd32f-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd32f-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="bd32f-110">Cell name:</span></span>  <br/> | <span data-ttu-id="bd32f-111">Width</span><span class="sxs-lookup"><span data-stu-id="bd32f-111">Width</span></span>  <br/> |
   
<span data-ttu-id="bd32f-112">プログラムから、インデックスによって [Width] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd32f-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd32f-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd32f-113">Section index:</span></span>  <br/> |<span data-ttu-id="bd32f-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bd32f-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bd32f-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd32f-115">Row index:</span></span>  <br/> |<span data-ttu-id="bd32f-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="bd32f-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="bd32f-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd32f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="bd32f-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="bd32f-118">**visXFormWidth**</span></span> <br/> |
   

