---
title: '[PageRightMargin] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: 印刷ページの右余白を指定します。
ms.openlocfilehash: d30669626fe07379521d61554010ae1bd7b0e83a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440011"
---
# <a name="pagerightmargin-cell-print-properties-section"></a><span data-ttu-id="39d0f-103">[PageRightMargin] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="39d0f-103">PageRightMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="39d0f-104">印刷ページの右余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="39d0f-104">Specifies the margin on the right of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39d0f-105">注釈</span><span class="sxs-lookup"><span data-stu-id="39d0f-105">Remarks</span></span>

<span data-ttu-id="39d0f-p101">この値は物理単位を表し、縮尺または図面の単位には影響されません。たとえば、このセルの値が 0.25 インチなら、ページ単位がフィートの場合でも、この余白は 0.25 インチです。単位が明示されていない場合、既定ではこの値にページ単位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="39d0f-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="39d0f-109">別の数式または **CellsU** を使用したプログラムから、名前による [PageRightMargin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="39d0f-109">To get a reference to the PageRightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="39d0f-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="39d0f-110">Cell name:</span></span>  <br/> | <span data-ttu-id="39d0f-111">PageRightMargin</span><span class="sxs-lookup"><span data-stu-id="39d0f-111">PageRightMargin</span></span>  <br/> |
   
<span data-ttu-id="39d0f-112">プログラムから、インデックスによる [PageRightMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="39d0f-112">To get a reference to the PageRightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="39d0f-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="39d0f-113">Section index:</span></span>  <br/> |<span data-ttu-id="39d0f-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="39d0f-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="39d0f-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="39d0f-115">Row index:</span></span>  <br/> |<span data-ttu-id="39d0f-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="39d0f-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="39d0f-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="39d0f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="39d0f-118">**visPrintPropertiesRightMargin**</span><span class="sxs-lookup"><span data-stu-id="39d0f-118">**visPrintPropertiesRightMargin**</span></span> <br/> |
   

