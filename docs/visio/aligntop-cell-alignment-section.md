---
title: '[AlignTop] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50
localization_priority: Normal
ms.assetid: 56e0b544-8504-0fbb-5810-7cf94d775f7c
description: 親図形の原点を基準として、図形の上部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。
ms.openlocfilehash: a52527b8a0ef6398f475b3d6241e03afa6cd697b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406697"
---
# <a name="aligntop-cell-alignment-section"></a><span data-ttu-id="55573-103">[AlignTop] セル ([Alignment] セクション)</span><span class="sxs-lookup"><span data-stu-id="55573-103">AlignTop Cell (Alignment Section)</span></span>

<span data-ttu-id="55573-104">親図形の原点を基準として、図形の上部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="55573-104">Determines the vertical position, relative to the origin of its parent, of a horizontal guide or guide point to which the shape's top border is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="55573-105">注釈</span><span class="sxs-lookup"><span data-stu-id="55573-105">Remarks</span></span>

<span data-ttu-id="55573-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignTop] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="55573-106">To get a reference to the AlignTop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55573-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="55573-107">Cell name:</span></span>  <br/> | <span data-ttu-id="55573-108">AlignTop</span><span class="sxs-lookup"><span data-stu-id="55573-108">AlignTop</span></span>  <br/> |
   
<span data-ttu-id="55573-109">プログラムから、インデックスによって [AlignTop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="55573-109">To get a reference to the AlignTop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55573-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="55573-110">Section index:</span></span>  <br/> |<span data-ttu-id="55573-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="55573-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="55573-112">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="55573-112">Row index:</span></span>  <br/> |<span data-ttu-id="55573-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="55573-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="55573-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="55573-114">Cell index:</span></span>  <br/> |<span data-ttu-id="55573-115">**visAlignTop**</span><span class="sxs-lookup"><span data-stu-id="55573-115">**visAlignTop**</span></span> <br/> |
   

