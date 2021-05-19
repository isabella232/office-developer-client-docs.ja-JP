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
description: 選択した図形の幅を図面の単位で表した値が表示されます。1-D 図形の幅を決定する既定の数式は次のとおりです。
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415195"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="b7c3c-104">[Width] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="b7c3c-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="b7c3c-p102">選択した図形の幅を図面の単位で表した値が表示されます。1-D 図形の幅を決定する既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b7c3c-p102">Contains the width of the selected shape in drawing units. The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="b7c3c-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="b7c3c-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7c3c-108">注釈</span><span class="sxs-lookup"><span data-stu-id="b7c3c-108">Remarks</span></span>

<span data-ttu-id="b7c3c-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Width] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b7c3c-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7c3c-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="b7c3c-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b7c3c-111">Width</span><span class="sxs-lookup"><span data-stu-id="b7c3c-111">Width</span></span>  <br/> |
   
<span data-ttu-id="b7c3c-112">プログラムから、インデックスによって [Width] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7c3c-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7c3c-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b7c3c-113">Section index:</span></span>  <br/> |<span data-ttu-id="b7c3c-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b7c3c-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b7c3c-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b7c3c-115">Row index:</span></span>  <br/> |<span data-ttu-id="b7c3c-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="b7c3c-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="b7c3c-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b7c3c-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b7c3c-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="b7c3c-118">**visXFormWidth**</span></span> <br/> |
   

