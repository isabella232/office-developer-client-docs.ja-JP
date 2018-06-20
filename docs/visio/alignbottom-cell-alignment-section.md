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
ms.openlocfilehash: 959a6a5a6e380a84e85d1d2c2c954b89a4eb6f99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804784"
---
# <a name="alignbottom-cell-alignment-section"></a><span data-ttu-id="e0999-103">[AlignBottom] セル ([Alignment] セクション)</span><span class="sxs-lookup"><span data-stu-id="e0999-103">AlignBottom Cell (Alignment Section)</span></span>

<span data-ttu-id="e0999-104">親図形の原点を基準として、図形の下部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0999-104">Determines the vertical position, relative to the origin of its parent, of a horizontal guide or guide point to which the shape's bottom border is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0999-105">備考</span><span class="sxs-lookup"><span data-stu-id="e0999-105">Remarks</span></span>

<span data-ttu-id="e0999-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって (下揃え) のセルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e0999-106">To get a reference to the AlignBottom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e0999-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="e0999-107">Cell name:</span></span>  <br/> | <span data-ttu-id="e0999-108">(下揃え)</span><span class="sxs-lookup"><span data-stu-id="e0999-108">AlignBottom</span></span>  <br/> |
   
<span data-ttu-id="e0999-109">プログラムから、インデックスによって [(下揃え) のセルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e0999-109">To get a reference to the AlignBottom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e0999-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e0999-110">Section index:</span></span>  <br/> |<span data-ttu-id="e0999-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e0999-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e0999-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e0999-112">Row index:</span></span>  <br/> |<span data-ttu-id="e0999-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="e0999-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="e0999-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e0999-114">Cell index:</span></span>  <br/> |<span data-ttu-id="e0999-115">**visAlignBottom**</span><span class="sxs-lookup"><span data-stu-id="e0999-115">**visAlignBottom**</span></span> <br/> |
   

