---
title: '[AlignLeft] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm30
localization_priority: Normal
ms.assetid: d094411e-ed65-1d0d-5c35-68b003da2696
description: 親図形の原点を基準として、図形の左辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。
ms.openlocfilehash: 5fdf1251c8829fd644d1a4bfd5eab8890c0d3e71
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346544"
---
# <a name="alignleft-cell-alignment-section"></a><span data-ttu-id="a72fd-103">[AlignLeft] セル ([Alignment] セクション)</span><span class="sxs-lookup"><span data-stu-id="a72fd-103">AlignLeft Cell (Alignment Section)</span></span>

<span data-ttu-id="a72fd-104">親図形の原点を基準として、図形の左辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="a72fd-104">Determines the horizontal position, relative to the origin of its parent, of a vertical guide or guide point to which the shape's left border is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a72fd-105">解説</span><span class="sxs-lookup"><span data-stu-id="a72fd-105">Remarks</span></span>

<span data-ttu-id="a72fd-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignLeft] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a72fd-106">To get a reference to the AlignLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a72fd-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="a72fd-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a72fd-108">[alignleft]</span><span class="sxs-lookup"><span data-stu-id="a72fd-108">AlignLeft</span></span>  <br/> |
   
<span data-ttu-id="a72fd-109">プログラムから、インデックスによって [AlignLeft] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a72fd-109">To get a reference to the AlignLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a72fd-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a72fd-110">Section index:</span></span>  <br/> |<span data-ttu-id="a72fd-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a72fd-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a72fd-112">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="a72fd-112">Row index:</span></span>  <br/> |<span data-ttu-id="a72fd-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="a72fd-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="a72fd-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a72fd-114">Cell index:</span></span>  <br/> |<span data-ttu-id="a72fd-115">**visAlignLeft**</span><span class="sxs-lookup"><span data-stu-id="a72fd-115">**visAlignLeft**</span></span> <br/> |
   

