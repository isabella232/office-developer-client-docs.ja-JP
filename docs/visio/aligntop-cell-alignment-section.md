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
ms.openlocfilehash: 399514aa95897348238008715ee92694d57bad96
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804791"
---
# <a name="aligntop-cell-alignment-section"></a><span data-ttu-id="7c51c-103">[AlignTop] セル ([Alignment] セクション)</span><span class="sxs-lookup"><span data-stu-id="7c51c-103">AlignTop Cell (Alignment Section)</span></span>

<span data-ttu-id="7c51c-104">親図形の原点を基準として、図形の上部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="7c51c-104">Determines the vertical position, relative to the origin of its parent, of a horizontal guide or guide point to which the shape's top border is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c51c-105">備考</span><span class="sxs-lookup"><span data-stu-id="7c51c-105">Remarks</span></span>

<span data-ttu-id="7c51c-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [aligntop] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="7c51c-106">To get a reference to the AlignTop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c51c-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="7c51c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="7c51c-108">[Aligntop]</span><span class="sxs-lookup"><span data-stu-id="7c51c-108">AlignTop</span></span>  <br/> |
   
<span data-ttu-id="7c51c-109">プログラムから、インデックスによって [aligntop] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c51c-109">To get a reference to the AlignTop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c51c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7c51c-110">Section index:</span></span>  <br/> |<span data-ttu-id="7c51c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7c51c-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7c51c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7c51c-112">Row index:</span></span>  <br/> |<span data-ttu-id="7c51c-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="7c51c-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="7c51c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7c51c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="7c51c-115">**visAlignTop**</span><span class="sxs-lookup"><span data-stu-id="7c51c-115">**visAlignTop**</span></span> <br/> |
   

