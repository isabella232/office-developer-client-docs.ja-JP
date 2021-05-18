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
ms.openlocfilehash: 6249c994299582d52a7f54a0c75370851dfad498
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421460"
---
# <a name="aligncenter-cell-alignment-section"></a><span data-ttu-id="e23e2-103">[AlignCenter] セル ([Alignment] セクション)</span><span class="sxs-lookup"><span data-stu-id="e23e2-103">AlignCenter Cell (Alignment Section)</span></span>

<span data-ttu-id="e23e2-104">親図形の原点を基準として、図形の水平方向の中心を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="e23e2-104">Determines the horizontal position, relative to the origin of its parent, of a vertical guide or guide point to which the shape's horizontal center is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e23e2-105">注釈</span><span class="sxs-lookup"><span data-stu-id="e23e2-105">Remarks</span></span>

<span data-ttu-id="e23e2-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignCenter] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e23e2-106">To get a reference to the AlignCenter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e23e2-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="e23e2-107">Cell name:</span></span>  <br/> | <span data-ttu-id="e23e2-108">AlignCenter</span><span class="sxs-lookup"><span data-stu-id="e23e2-108">AlignCenter</span></span>  <br/> |
   
<span data-ttu-id="e23e2-109">プログラムから、インデックスによって [AlignCenter] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e23e2-109">To get a reference to the AlignCenter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e23e2-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e23e2-110">Section index:</span></span>  <br/> |<span data-ttu-id="e23e2-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e23e2-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e23e2-112">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="e23e2-112">Row index:</span></span>  <br/> |<span data-ttu-id="e23e2-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="e23e2-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="e23e2-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e23e2-114">Cell index:</span></span>  <br/> |<span data-ttu-id="e23e2-115">**visAlignCenter**</span><span class="sxs-lookup"><span data-stu-id="e23e2-115">**visAlignCenter**</span></span> <br/> |
   

