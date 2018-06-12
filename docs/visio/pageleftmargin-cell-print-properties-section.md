---
title: '[PageLeftMargin] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: 印刷ページの左余白を指定します。
ms.openlocfilehash: 5fd2c8cd5b18a4baedd355627005b7c5c2df3252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805953"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="ee24a-103">[PageLeftMargin] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="ee24a-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="ee24a-104">印刷ページの左余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="ee24a-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee24a-105">備考</span><span class="sxs-lookup"><span data-stu-id="ee24a-105">Remarks</span></span>

<span data-ttu-id="ee24a-p101">この値は物理単位を表し、縮尺または図面の単位には影響されません。たとえば、このセルの値が 0.25 インチなら、ページ単位がフィートの場合でも、この余白は 0.25 インチです。単位が明示されていない場合、既定ではこの値にページ単位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee24a-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="ee24a-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PageLeftMargin] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ee24a-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee24a-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ee24a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ee24a-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="ee24a-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="ee24a-112">プログラムから、インデックスによって [PageLeftMargin] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee24a-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee24a-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee24a-113">Section index:</span></span>  <br/> |<span data-ttu-id="ee24a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ee24a-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ee24a-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee24a-115">Row index:</span></span>  <br/> |<span data-ttu-id="ee24a-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="ee24a-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="ee24a-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee24a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ee24a-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="ee24a-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

