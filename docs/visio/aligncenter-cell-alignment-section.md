---
title: '[AlignCenter] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm25
localization_priority: Normal
ms.assetid: 7d4416b2-429b-713e-61dc-8b2ead0e6053
description: 親図形の原点を基準として、図形の水平方向の中心を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。
ms.openlocfilehash: 342385dc2d08efd95e8dbad9d96ab59b2133ed7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804761"
---
# <a name="aligncenter-cell-alignment-section"></a><span data-ttu-id="1dd45-103">[AlignCenter] セル ([配置] セクション)</span><span class="sxs-lookup"><span data-stu-id="1dd45-103">AlignCenter Cell (Alignment Section)</span></span>

<span data-ttu-id="1dd45-104">親図形の原点を基準として、図形の水平方向の中心を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="1dd45-104">Determines the horizontal position, relative to the origin of its parent, of a vertical guide or guide point to which the shape's horizontal center is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1dd45-105">備考</span><span class="sxs-lookup"><span data-stu-id="1dd45-105">Remarks</span></span>

<span data-ttu-id="1dd45-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignCenter] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1dd45-106">To get a reference to the AlignCenter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1dd45-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="1dd45-107">Cell name:</span></span>  <br/> | <span data-ttu-id="1dd45-108">AlignCenter</span><span class="sxs-lookup"><span data-stu-id="1dd45-108">AlignCenter</span></span>  <br/> |
   
<span data-ttu-id="1dd45-109">プログラムから、インデックスによって [AlignCenter] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1dd45-109">To get a reference to the AlignCenter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1dd45-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1dd45-110">Section index:</span></span>  <br/> |<span data-ttu-id="1dd45-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1dd45-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1dd45-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1dd45-112">Row index:</span></span>  <br/> |<span data-ttu-id="1dd45-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="1dd45-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="1dd45-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1dd45-114">Cell index:</span></span>  <br/> |<span data-ttu-id="1dd45-115">**visAlignCenter**</span><span class="sxs-lookup"><span data-stu-id="1dd45-115">**visAlignCenter**</span></span> <br/> |
   

