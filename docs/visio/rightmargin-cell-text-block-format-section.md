---
title: '[RightMargin] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。 既定値は 0.1 インチです。
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326776"
---
# <a name="rightmargin-cell-text-block-format-section"></a><span data-ttu-id="c733e-104">[RightMargin] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="c733e-104">RightMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="c733e-105">テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="c733e-105">Determines the distance between the right border of the text block and the text it contains.</span></span> <span data-ttu-id="c733e-106">既定値は 0.1 インチです。</span><span class="sxs-lookup"><span data-stu-id="c733e-106">The default is 0.1 inch.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c733e-107">解説</span><span class="sxs-lookup"><span data-stu-id="c733e-107">Remarks</span></span>

<span data-ttu-id="c733e-p103">この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右余白は変わりません。</span><span class="sxs-lookup"><span data-stu-id="c733e-p103">This value is independent of the scale of the drawing. If the drawing is scaled, the right margin remains the same.</span></span>
  
<span data-ttu-id="c733e-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [RightMargin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c733e-110">To get a reference to the RightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c733e-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="c733e-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c733e-112">RightMargin</span><span class="sxs-lookup"><span data-stu-id="c733e-112">RightMargin</span></span>  <br/> |
   
<span data-ttu-id="c733e-113">プログラムから、インデックスによって [RightMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c733e-113">To get a reference to the RightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c733e-114">セクション インデックス :</span><span class="sxs-lookup"><span data-stu-id="c733e-114">Section index:</span></span>  <br/> |<span data-ttu-id="c733e-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c733e-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c733e-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c733e-116">Row index:</span></span>  <br/> |<span data-ttu-id="c733e-117">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="c733e-117">**visRowText**</span></span> <br/> |
| <span data-ttu-id="c733e-118">セル インデックス :</span><span class="sxs-lookup"><span data-stu-id="c733e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c733e-119">**visTxtBlkRightMargin**</span><span class="sxs-lookup"><span data-stu-id="c733e-119">**visTxtBlkRightMargin**</span></span> <br/> |
   

