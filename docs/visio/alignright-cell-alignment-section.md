---
title: '[AlignRight] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251297
localization_priority: Normal
ms.assetid: c6d298a4-1602-a53c-bb5d-2ef16b43f722
description: 親図形の原点を基準として、図形の右辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。
ms.openlocfilehash: 558808908107a3e42d9d6e4a6fc1cf177150edb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439773"
---
# <a name="alignright-cell-alignment-section"></a><span data-ttu-id="c18c8-103">[AlignRight] セル ([Alignment] セクション)</span><span class="sxs-lookup"><span data-stu-id="c18c8-103">AlignRight Cell (Alignment Section)</span></span>

<span data-ttu-id="c18c8-104">親図形の原点を基準として、図形の右辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="c18c8-104">Determines the horizontal position, relative to the origin of its parent, of a vertical guide or guide point to which the shape's right border is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c18c8-105">注釈</span><span class="sxs-lookup"><span data-stu-id="c18c8-105">Remarks</span></span>

<span data-ttu-id="c18c8-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignRight] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c18c8-106">To get a reference to the AlignRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c18c8-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="c18c8-107">Cell name:</span></span>  <br/> | <span data-ttu-id="c18c8-108">AlignRight</span><span class="sxs-lookup"><span data-stu-id="c18c8-108">AlignRight</span></span>  <br/> |
   
<span data-ttu-id="c18c8-109">プログラムから、インデックスによって [AlignRight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c18c8-109">To get a reference to the AlignRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c18c8-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c18c8-110">Section index:</span></span>  <br/> |<span data-ttu-id="c18c8-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c18c8-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c18c8-112">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="c18c8-112">Row index:</span></span>  <br/> |<span data-ttu-id="c18c8-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="c18c8-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="c18c8-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c18c8-114">Cell index:</span></span>  <br/> |<span data-ttu-id="c18c8-115">**visAlignRight**</span><span class="sxs-lookup"><span data-stu-id="c18c8-115">**visAlignRight**</span></span> <br/> |
   

