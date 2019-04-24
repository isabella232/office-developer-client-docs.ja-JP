---
title: '[Color] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: 図面校閲者のマークアップに割り当てられている色を表す RGB 値。
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341819"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="95ef9-103">[Color] セル ([Reviewer] セクション)</span><span class="sxs-lookup"><span data-stu-id="95ef9-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="95ef9-104">図面校閲者のマークアップに割り当てられている色を表す RGB 値。</span><span class="sxs-lookup"><span data-stu-id="95ef9-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="95ef9-105">解説</span><span class="sxs-lookup"><span data-stu-id="95ef9-105">Remarks</span></span>

<span data-ttu-id="95ef9-p101">色は、赤、青、緑、紫、オレンジ、青緑、グレーの順番で校閲者に割り当てられます。校閲者がそれ以上いる場合には、再度先頭から順番に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="95ef9-p101">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray. These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="95ef9-108">オリジナルの図面ページに記入されたコメントは、[Color] セルで校閲者に割り当てた色にかかわらず常に黄色です。</span><span class="sxs-lookup"><span data-stu-id="95ef9-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="95ef9-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="95ef9-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95ef9-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="95ef9-110">Cell name:</span></span>  <br/> | <span data-ttu-id="95ef9-111">校閲者の色 [ *i* ] *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="95ef9-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="95ef9-112">プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="95ef9-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95ef9-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="95ef9-113">Section index:</span></span>  <br/> |<span data-ttu-id="95ef9-114">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="95ef9-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="95ef9-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="95ef9-115">Row index:</span></span>  <br/> |<span data-ttu-id="95ef9-116">**visRowReviewer** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="95ef9-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="95ef9-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="95ef9-117">Cell index:</span></span>  <br/> |<span data-ttu-id="95ef9-118">**visReviewerColor**</span><span class="sxs-lookup"><span data-stu-id="95ef9-118">**visReviewerColor**</span></span> <br/> |
   

