---
title: '[AlignMiddle] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm40
localization_priority: Normal
ms.assetid: 444bf9e2-80e8-cbe5-6855-b445f16e7920
description: 親図形の原点を基準として、図形の垂直方向の中心を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。
ms.openlocfilehash: dd982f716fdd98c684b1668063516de07eb965e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804783"
---
# <a name="alignmiddle-cell-alignment-section"></a><span data-ttu-id="04b5d-103">[AlignMiddle] セル ([配置] セクション)</span><span class="sxs-lookup"><span data-stu-id="04b5d-103">AlignMiddle Cell (Alignment Section)</span></span>

<span data-ttu-id="04b5d-104">親図形の原点を基準として、図形の垂直方向の中心を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="04b5d-104">Determines the vertical position, relative to the origin of its parent, of a horizontal guide or guide point to which the shape's vertical center is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="04b5d-105">備考</span><span class="sxs-lookup"><span data-stu-id="04b5d-105">Remarks</span></span>

<span data-ttu-id="04b5d-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignMiddle] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="04b5d-106">To get a reference to the AlignMiddle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04b5d-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="04b5d-107">Cell name:</span></span>  <br/> | <span data-ttu-id="04b5d-108">AlignMiddle</span><span class="sxs-lookup"><span data-stu-id="04b5d-108">AlignMiddle</span></span>  <br/> |
   
<span data-ttu-id="04b5d-109">プログラムから、インデックスによって [AlignMiddle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="04b5d-109">To get a reference to the AlignMiddle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04b5d-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="04b5d-110">Section index:</span></span>  <br/> |<span data-ttu-id="04b5d-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="04b5d-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="04b5d-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="04b5d-112">Row index:</span></span>  <br/> |<span data-ttu-id="04b5d-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="04b5d-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="04b5d-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="04b5d-114">Cell index:</span></span>  <br/> |<span data-ttu-id="04b5d-115">**visAlignMiddle**</span><span class="sxs-lookup"><span data-stu-id="04b5d-115">**visAlignMiddle**</span></span> <br/> |
   

