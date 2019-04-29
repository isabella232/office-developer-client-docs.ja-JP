---
title: '[AlignBottom] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm20
localization_priority: Normal
ms.assetid: 234e7ffa-04e3-0204-c5be-7ff7a4d0d54c
description: 親図形の原点を基準として、図形の下部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。
ms.openlocfilehash: 66fea9949f2f31eb5c3aaf43804ac0ec9f7e20fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411800"
---
# <a name="alignbottom-cell-alignment-section"></a><span data-ttu-id="87649-103">[AlignBottom] セル ([Alignment] セクション)</span><span class="sxs-lookup"><span data-stu-id="87649-103">AlignBottom Cell (Alignment Section)</span></span>

<span data-ttu-id="87649-104">親図形の原点を基準として、図形の下部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="87649-104">Determines the vertical position, relative to the origin of its parent, of a horizontal guide or guide point to which the shape's bottom border is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87649-105">注釈</span><span class="sxs-lookup"><span data-stu-id="87649-105">Remarks</span></span>

<span data-ttu-id="87649-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignBottom] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="87649-106">To get a reference to the AlignBottom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87649-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="87649-107">Cell name:</span></span>  <br/> | <span data-ttu-id="87649-108">alignbottom]</span><span class="sxs-lookup"><span data-stu-id="87649-108">AlignBottom</span></span>  <br/> |
   
<span data-ttu-id="87649-109">プログラムから、インデックスによって [AlignBottom] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="87649-109">To get a reference to the AlignBottom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87649-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="87649-110">Section index:</span></span>  <br/> |<span data-ttu-id="87649-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87649-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="87649-112">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="87649-112">Row index:</span></span>  <br/> |<span data-ttu-id="87649-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="87649-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="87649-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="87649-114">Cell index:</span></span>  <br/> |<span data-ttu-id="87649-115">**visAlignBottom**</span><span class="sxs-lookup"><span data-stu-id="87649-115">**visAlignBottom**</span></span> <br/> |
   

