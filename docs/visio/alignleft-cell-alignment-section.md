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
ms.openlocfilehash: f2fc7ef62723812f7dde3f94272a90927272936e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804765"
---
# <a name="alignleft-cell-alignment-section"></a><span data-ttu-id="6bd1c-103">[AlignLeft] セル ([Alignment] セクション)</span><span class="sxs-lookup"><span data-stu-id="6bd1c-103">AlignLeft Cell (Alignment Section)</span></span>

<span data-ttu-id="6bd1c-104">親図形の原点を基準として、図形の左辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="6bd1c-104">Determines the horizontal position, relative to the origin of its parent, of a vertical guide or guide point to which the shape's left border is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6bd1c-105">備考</span><span class="sxs-lookup"><span data-stu-id="6bd1c-105">Remarks</span></span>

<span data-ttu-id="6bd1c-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [alignleft] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="6bd1c-106">To get a reference to the AlignLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6bd1c-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="6bd1c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="6bd1c-108">[Alignleft]</span><span class="sxs-lookup"><span data-stu-id="6bd1c-108">AlignLeft</span></span>  <br/> |
   
<span data-ttu-id="6bd1c-109">プログラムから、インデックスによって [alignleft] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6bd1c-109">To get a reference to the AlignLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6bd1c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6bd1c-110">Section index:</span></span>  <br/> |<span data-ttu-id="6bd1c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6bd1c-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6bd1c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6bd1c-112">Row index:</span></span>  <br/> |<span data-ttu-id="6bd1c-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="6bd1c-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="6bd1c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6bd1c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="6bd1c-115">**visAlignLeft**</span><span class="sxs-lookup"><span data-stu-id="6bd1c-115">**visAlignLeft**</span></span> <br/> |
   

